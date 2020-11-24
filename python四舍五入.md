###python四舍五入
1. python四舍五入损失精度
  * Decimal、quantize
  * ROUND_HALF_UP(>0)、ROUND_HALF_DOWN(<0)
  * DecimalException
 ```
return Decimal(str(x)).quantize(Decimal(n), ROUND_HALF_UP)
return Decimal(str(x)).quantize(Decimal(n), ROUND_HALF_DOWN)
 ```
