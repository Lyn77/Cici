###mongodb表关联
1. 多个外键
```
{
            $lookup: {
                from: '从表',
                let: {
                    name: '$主表key',
                    anme: '$主表key'
                },
                pipeline: [
                    {
                        $match: {
                            $expr: {
                                $and: [
                                    {
                                        $eq: [
                                            '$从表key',
                                            '$$主表name'
                                        ]
                                    },
                                    {
                                        $eq: [
                                            '$从表key',
                                            '$$主表name'
                                        ]
                                    }
                                ]
                            }
                        }
                    }
                ],
            }
        },
```
