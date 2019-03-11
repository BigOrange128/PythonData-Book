## 部分索引索引对象的方法和属性

    函数名                 描述
    
    append                 将额外的索引对象粘贴到原索引后，产生一个新的索引
    difference             计算两个索引的差集
    intersection           计算两个索引的交集
    union                  计算两个索引的并集
    isin                   计算表示每一个值是否在传值容器中的布尔数组
    delete                 将位置i的元素删除，并产生新的索引
    drop                   根据传参删除指定索引值，并产生新的索引
    is_monotonic           如果索引序列递增则返回True
    is_unique              如果索引序列唯一则返回True
    unique                 计算索引的唯一值序列
## reindex方法的参数
>reindex用于重建索引 

    参数                   描述
    
    index                  新建作为索引的序列，可以是索引实例或任意其他序列型Python数据结构，索引使用时无需复制
    method                 插值方式;'ffill'为前向填充，而'bfill'是后向填充
    fill_value             通过重新索引引入缺失数据时使用的替代值
    limit                  当前向或后向填充时，所需填充的最大尺寸间隙(以元素数量)
    tolerance              当前向或后向填充时，所需填充的不精确匹配下的最大尺寸间隙(以绝对数字距离)
    level                  匹配MultiIndex级别的简单索引；否则选择子集
    copy                   如果为True，即使新索引等于旧索引，也总是复制底层数据；如果是False，则在索引相同时不要复制数据
## DataFrame索引选项
    
    类型                      描述
    
    df[val]                   从DataFrame中选择单列或列序列；特殊情况的便利：布尔数组(过滤行)，切片(切片行)或布尔值DataFrame(根据某些标准设置的值)
    df.loc[val]               根据标签选择DataFrame的单行或多行
    df.loc[:, val]            根据标签选择单列或多列
    df.loc[val1, val2]        同时选择行和列的一部分
    df.iloc[where]            根据整数位置选择单列或多行
    df.iloc[:, where]         根据整数位置选择单列或多列
    df.iloc[where_i, where_j] 根据整数位置选择行和列
    df.at[label_i, label_j]   根据行、列标签选择单个标量值
    df.iat[i, j]              根据行、列整数位置选择单个标量值
    reindex方法               通过标签选择行或列
    get_value, set_value方法  根据行和列的标签设置单个值
    
## 灵活算数方法
> df1.add(df2), pd.DataFrame.add(df1, df2)
    
    方法名                 描述
    
    add, radd              加法(+)
    sub, rsub              减法(-)
    div, rdiv              除法(/)
    floordiv, rfloordiv    整除(//)
    mul, rmul              乘法(*)
    pow, rpow              幂次方(**)
## 排名中平级关系打破方法
    
    方法                   描述
    
    average                默认：在每个组中分配平均排名
    min                    对整个组使用最小排名
    max                    对整个组使用最大排名
    first                  按照值在数据中出现的次序分配排名
    dense                  类似于method = 'min'，但组间排名总是增加1，而不是一个组中的相等元素的数量
## 规约方法可选参数   

    参数                  描述
    
    axis                  归约轴，0为行向，1为列向
    skipna                排除缺失值，默认为True
    level                 如果轴是多层索引的(MultiIndex)，该参数可以缩减分组层级
    
## 描述性统计和汇总统计

    方法                   描述
    
    count                  非NA值的个数
    describe               计算Series或DataFrame各列的汇总统计集合
    min, max               计算最小值、最大值
    argmin, argmax         分别计算最小值、最大值所在的索引位置(整数)
    idxmin, idxmax         分别计算最小值或最大值所在的索引标签
    quantile               计算样本的从0到1间的分位数
    sum                    加和
    mean                   均值
    median                 中位数(50%分位数)
    mad                    平均值的平均绝对偏差
    prod                   所有值的积
    var                    值的样本方差
    std                    值的样本标准差
    skew                   样本偏度(第三时刻)值
    kurt                   样本峰度(第四时刻)值
    cumsum                 累计值
    cummin, cummax         累计值的最小值或最大值
    cumprod                值的累计积
    diff                   计算第一个算数差值(对时间序列有用)
    pct_change             计算百分比
      
## 唯一值、计数、和集合成员属性方法

    方法                    描述
    
    isin                    计算表征Series中每个值是否包含于传入序列的布尔值数组
    match                   计算数组中每个值的整数索引，形成一个唯一值数组。有助于数据对齐和join类型的操作
    unique                  计算Series值中的唯一值数组，按照观察顺序返回
    value_counts            返回一个Series，索引是唯一值序列，值是计算个数，按照个数降序排序
