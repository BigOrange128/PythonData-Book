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
> np.add(arr1, arr2)

    函数名                  描述
    
    add                     将数组的对应元素相加
    subtract                在第二个数组中，将第一个数组中包含的元素去除
    multiply                将数组的对应元素相乘
    divide, floor_divide    除或整除(放弃余数)
    power                   将第二个数组的元素作为第一个数组对应元素的幂次方
    maximum, fmax           逐个元素计算最大值，fmax忽略NaN
    minimum, fmin           逐个元素计算最小值，fmin忽略NaN
    mod                     按元素的求模计算(即求除法的余数)
    copysign                将第一个数组的符号值改为第二个数组的符号值
    
    greater, greater_equal, 进行逐个元素的比较，返回布尔值数组 (与数学操作符号>、>=、<、<=、==、!=效果一致)   
    less, less_equal,equal,   
    not_equal
    
    logical_and,logical_or, 进行逐个元素的逻辑操作(与逻辑操作符&、|、^效果一致)
    logical_xor
## 基础数学统计方法 
> arr.sum()    通过传递axis=0, 1可以改变计算轴向为行或列

    方法名                   描述
    
    sum                     沿着轴向计算所有元素的累和，0长度的数组，累和为0
    mean                    数学平均，0长度的数组平均值为NaN
    std，var                标准差和方差，可以选择自由调度(默认分母是n)
    min，max                最小值和最大值
    argmin，argmax          最小值和最大值的位置
    cumsum                  从0开始元素累积和
    cumprod                 从1开始元素累积积
## 数组的集合操作
    方法名                   描述
    
    unique(x)               计算x的唯一值，并排序
    intersectld(x, y)       计算x和y的交集，并排序
    unionld(x, y)           计算x和y的并集，并排序
    inld(x, y)              计算x中的元素是否包含在y中，返回一个布尔值数组
    setdiffld(x, y)         差集，在x中但不在y中的x的元素
    setxorld(x, y)          异或集，在x中或y中，但不属于x、y交集的元素    
## 常用numpy.linalg函数
> dot(x, y)   x.dot(y)

    函数名                  描述
    
    diag                   将一个方阵的对角(或非对角)元素作为一维数组返回，或者将一维数组转换成一个方阵，并且在非对角线上有零点
    dot                    矩阵点乘
    trace                  计算对角元素和
    det                    计算矩阵的行列式
    eig                    计算方阵的特征值和特征向量
    inv                    计算方阵的逆矩阵
    pinv                   计算矩阵的Moore-Penrose伪逆
    qr                     计算QR分解
    svd                    计算奇异值分解(SVD)
    solve                  求解x的线性系统Ax = b，其中A是方阵
    lstsq                  计算Ax = b的最小二乘解
                    
## numpy.random部分函数
> np.random.seed(1234)

    函数名                  描述
    
    seed                    向随机数生成器传递随机状态种子
    permutation             返回一个序列的随机排序，或者返回一个乱序的整数范围序列
    shuffle                 随机排列一个序列
    rand                    从均匀分布中抽取样本
    randint                 根据给定的由低到高的范围抽取随机整数
    randn                   从均值0方差1的正态分布中抽取样本(MATLAB型接口)
    binomial                从二项分布中抽取样本
    normal                  从正态(高斯)分布中抽取样本
    beta                    从beta分布中抽取样本
    chisquare               从卡方分布中抽取样本
    gamma                   从伽马分布中抽取样本
    uniform                 从均匀[0, 1)分布中抽取样本
    
