###python四舍五入
1. python四舍五入损失精度
  * Decimal、quantize
  * ROUND_HALF_UP(>0)、ROUND_HALF_DOWN(<0)
  * DecimalException
 ```
 try: 
        if x > 0:
            return Decimal(str(x)).quantize(Decimal(n), ROUND_HALF_UP)
        else:
            return Decimal(str(x)).quantize(Decimal(n), ROUND_HALF_DOWN)
    except DecimalException as e:
        return x
 ```
