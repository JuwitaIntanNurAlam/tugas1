import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
from sklearn.cluster import KMeans
Dataset = pd.read_csv('konsumen2.csv')
Dataset.keys()
Index(['Gaji', 'Pengeluaran'], dtype='object')
# Melakukan Coding disini
dataku = pd.DataFrame(Dataset)
dataku.head()
Gaji	Pengeluaran
0	2500	1750
1	3800	4200
2	3900	3800
3	4350	5500
4	4400	3200
# Konversi ke data array
x = np.array(Dataset)
print(x)
[[ 2500  1750]
 [ 3800  4200]
 [ 3900  3800]
 [ 4350  5500]
 [ 4400  3200]
 [ 5500  5450]
 [ 5600  5950]
 [ 5750  4100]
 [ 6850  6050]
 [ 6900  8500]
 [ 7250  9500]
 [ 7350  6050]
 [ 7500  8500]
 [ 7800  9500]
 [ 8200  8300]
 [ 8500  6500]
 [ 8550  8400]
 [ 8750  6000]
 [ 9100 10500]
 [ 9100  8500]]
# Menampilkan data dalam bentuk scatter plot
plt.scatter(x[:,0],x[:,1], label="True Position")
plt.xlabel("Gaji")
plt.ylabel("Pengeluaran")
plt.title("Grafik konsumen")
plt.show()
