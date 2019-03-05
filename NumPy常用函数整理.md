## 数组生成函数
> np.array(data1)

    函数名     描述
    
    array      将输入数据转换为ndarray，默认复制所有输入数据
    asarray    将输入转换为ndarray，如果输入已经是ndarray则不再复制
    
    arange     Python内建函数range的数组版，返回一个数组
    
    ones       根据给定形状和数据类型生成全1数组  
    ones_like  根据所给的数组生成一个形状一样的全1数组
    
    zeros      根据给定形状和数据类型生成全0数组   
    zeros_like 根据所给的数组生成一个形状一样的全0数组
    
    empty      根据给定形状生成一个没有初始化数值的空数组  
    empty_like 根据所给数组生成一个形状一样但没有初始化值的空数组
    
    full       根据给定的形状和数据类型生成指定数值的数组
    full_like  根据所给的数组生成一个形状一样但内容是指定数值的数组
    
    eye, identity  生成一个NXN特征矩阵(对角线位置都是1，其余位置是0)
## 数据类型表
    类型              类型代码      描述
    
    int8, uint8       i1, u1       有符号和无符号的8数位整数
    int16, uint16     i2, u2       有符号和无符号的16数位整数
    int32, uint32     i4, u4       .....
    int64, unit64     i8,u8        .....
    
    float16           f2           半精度浮点数
    float32           f4或f        标准单精度浮点数；兼容C语言float
    float64           f8或d        标准双精度浮点数；兼容C double和Python float
    float128          f16或g       扩展精度浮点数   
    
    complex64         c8, c16, c32 分别基于32位、64、128位浮点数的复数
    complex128        
    complex256
    
    bool              ?             布尔值，存储True或False
    object            O             Python object类型
    string_           S             修正的ASC 丨丨字符串类型；
                                    例如生成一个长度为10的字符串类型，使用'S10'
    unicode_          U             修正的Unicode类型；
                                    生成...10...,...'U10'                                                   
## 一元通用函数
> np.abs(arr)

    函数名                 描述
    
    abs、fabs              逐元素地计算整数、浮点数或复数的绝对值
    sqrt                   计算每个元素的平方根(等同于arr ** 0.5) 
    square                 计算每个元素的平方(等同于arr ** 2)
    exp                    计算每个元素的自然指数值e ** x
    log、log10、           自然对数(e为底）、对数10为底
    log2、log1p            对数2为底、log(1 + x)
    sign                   计算每个元素的符号值：1(正数)、0(0)、-1(负数)
    ceil                   计算每个元素的最高整数值(即大于等于给定数值的最小整数)
    floor                  计算每个元素的最小整数值(即小于等于给定数值的最大整数)
    rint                   将元素保留到整数位，并保持dtype
    modf                   分别将数组的小数部分和整数部分按数组形式返回
    isnan                  返回数组中的元素是否是一个NaN(非数值)， 形式为布尔值数组
    isfinite、isinf        返回数组中的元素是否有限(非int、非NaN)、是否无限的，形式为布尔值数组
    cos、cosh、sin、       常规的双曲三角函数
    sinh、tan、tanh
    arccos、arccosh、      反三角函数
    arcsin、arcsinh、arctan、arctanh
    logical_not            对数组的元素按位取反(等同于~arr效果一致) 
## 二元通用函数

## 基础数学统计方法

## 数组的集合操作

## 常用numpy.linalg函数

## numpy.random部分函数
