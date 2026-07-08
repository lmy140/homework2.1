# homework2.1
# 任务1：创建(3,4) 0~9随机整数数组
arr = np.random.randint(0, 10, size=(3, 4))
print("原始数组 arr (3,4):")
print(arr)

# 任务2：reshape(4,3) 再转置
reshaped_arr = arr.reshape(4, 3).T
print("\n重塑+转置后数组:")
print(reshaped_arr)

# 任务3：布尔索引提取大于5的元素
filtered_arr = arr[arr > 5]
print("\n大于5的元素数组:")
print(filtered_arr)
print("原始数组：")
print(arr)

# 任务1：第2行（索引1）第1~3列 [5,6,7]
res1 = arr[1, 0:3]
print("\n1. 第2行1~3列：", res1)

# 任务2：所有行第3列（索引2）
res2 = arr[:, 2]
print("2. 全部行第3列：", res2)

# 任务3：步长切片取奇数行（第1、3行，索引0、2）
res3 = arr[::2, :]
print("3. 奇数行：")
print(res3)
import numpy as np
np.random.seed(42)

# 任务1：A、B (2,3) 逐元素乘 * 、矩阵乘 @
A = np.random.randint(1, 10, size=(2, 3))
B = np.random.randint(1, 10, size=(2, 3))
print("数组A：")
print(A)
print("数组B：")
print(B)

elem_mul = A * B       # 逐元素乘法
mat_mul = A @ B.T      # 矩阵乘法(2,3)@(3,2)=(2,2)
print("\n逐元素乘法 A * B：")
print(elem_mul)
print("矩阵乘法 A @ B.T：")
print(mat_mul)

# 任务2：[[1,2],[3,4]] 按行、列求和
mat = np.array([[1, 2], [3, 4]])
sum_col = np.sum(mat, axis=0)  # axis=0 列求和
sum_row = np.sum(mat, axis=1) # axis=1 行求和
print("\n原矩阵：")
print(mat)
print("按列求和(axis=0)：", sum_col)
print("按行求和(axis=1)：", sum_row)

# 任务3：均值、标准差、四舍五入
nums = np.array([1.2, 3.5, 2.8])
mean_val = np.mean(nums)
std_val = np.std(nums)
round_val = np.round(nums)
print("\n数组 [1.2,3.5,2.8]")
print("均值：", mean_val)
print("标准差：", std_val)
print("四舍五入：", round_val)
import numpy as np
np.random.seed(42)

# 任务1：长度10，0~1随机浮点，归一化到[0,100]
raw = np.random.rand(10)
min_raw = raw.min()
max_raw = raw.max()
# 归一化公式
norm_arr = (raw - min_raw) / (max_raw - min_raw) * 100

print("原始0~1浮点数组：")
print(raw)
print("\n归一化到0~100数组：")
print(norm_arr)

# 任务2：累计和、累计最大值
cumsum_arr = np.cumsum(norm_arr)
cummax_arr = np.maximum.accumulate(norm_arr)

print("\n累计和 cumsum：")
print(cumsum_arr)
print("累计最大值 cummax：")
print(cummax_arr)
