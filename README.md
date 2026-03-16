# Superstore Analysis
Proyek ini berfokus pada eksplorasi dan analisis dataset untuk menghasilkan insight yang bermakna dan mendukung pengambilan keputusan. Fokus utamanya adalah memahami data, melakukan berbagai analisis, dan memvisualisasikan temuan untuk mengomunikasikan hasil pengamatan secara efektif.

# Tentang Proyek Ini
Proyek ini memusatkan perhatian pada analisis komprehensif sebuah dataset yang mencakup berbagai aspek seperti penjualan, informasi pelanggan, detail produk, dan segmen pasar. Tugas-tugas utama yang dikerjakan meliputi pengecekan kualitas data, exploratory data analysis (EDA), analisis statistik, serta visualisasi tren dan pola dalam dataset.

# Tujuan
Tujuan utama proyek ini adalah mengekstrak insight yang dapat ditindaklanjuti dari dataset guna mendorong keputusan dan strategi bisnis. Melalui analisis dan visualisasi yang cermat, saya berupaya mengungkap tren, mengidentifikasi peluang, dan mengatasi tantangan yang ada dalam data.

# User Story
Sebagai data analis, saya memvalidasi dataset secara teliti untuk memastikan kualitas dan integritas data. Proses ini mencakup pengecekan missing values, duplikat, statistik deskriptif, dan memastikan format data sudah sesuai. Dengan memanfaatkan teknik analitik yang lebih canggih, saya berupaya mengungkap pola dan korelasi tersembunyi yang dapat memandu pengambilan keputusan strategis.

# Bagian Tambahan
- **Validasi Data:** Menjelaskan langkah-langkah yang dilakukan untuk memvalidasi dataset, termasuk memeriksa missing values, duplikat, statistik deskriptif, dan memastikan format data sudah tepat. [Klik Di Sini](#import-library)
- **Exploratory Data Analysis (EDA):** Menyajikan insight dari eksplorasi awal dataset, termasuk ringkasan statistik, distribusi, dan korelasi antar variabel.
- **Analisis Statistik:** Membahas uji statistik atau analisis yang dilakukan untuk memvalidasi temuan atau menguji hipotesis dalam dataset.
- **Visualisasi:** Menampilkan visualisasi yang dibuat untuk merepresentasikan insight dan tren utama yang ditemukan selama proses analisis.
- **Temuan Utama:** Merangkum temuan dan insight paling signifikan yang dihasilkan dari analisis, sekaligus menyoroti rekomendasi yang dapat ditindaklanjuti atau area yang perlu diteliti lebih lanjut.
- **Insight dan Solusi Bisnis:** Merefleksikan keseluruhan proses analisis, pelajaran yang dipetik, dan dampak insight terhadap potensi hasil bisnis. [Klik Di Sini](#findings-and-business-solution)

# EDA (Exploratory Data Analysis)
1. **Tren Penjualan dan Profit Tahunan:** Mengamati tren penjualan dan profit dari tahun ke tahun. [Klik Di Sini](#1-tren-penjualan-dan-profit-tahunan)
2. **Penjualan per Kategori Produk:** Mengidentifikasi kategori produk paling populer dan menampilkan 5 `product_name` teratas dari kategori tersebut. [Klik Di Sini](#2-penjualan-per-kategori-produk)
3. **Distribusi Metode Pengiriman:** Mengamati distribusi metode pengiriman yang digunakan. [Klik Di Sini](#3-distribusi-metode-pengiriman)
4. **Pendapatan per Negara/Wilayah:** Mengidentifikasi negara atau wilayah yang memberikan pendapatan tertinggi. [Klik Di Sini](#4-pendapatan-per-negarawilayah)
5. **Frekuensi Pembelian Pelanggan:** Memahami seberapa sering pelanggan melakukan pembelian. [Klik Di Sini](#5-frekuensi-pembelian-pelanggan)
6. **Distribusi Prioritas Pesanan:** Mengamati distribusi prioritas pesanan. [Klik Di Sini](#6-distribusi-prioritas-pesanan)
7. **Korelasi antara Diskon dan Profit:** Menentukan apakah ada korelasi antara jumlah diskon yang diberikan dengan profit yang diperoleh. [Klik Di Sini](#7-korelasi-antara-diskon-dan-profit)
8. **Profit Bulanan (Setelah Diskon):** Melihat profit per bulan untuk setiap tahun. [Klik Di Sini](#8-profit-bulanan-setelah-diskon)
9. **Rata-rata Profit (Setelah Diskon) per Pesanan:** Menghitung rata-rata profit dari setiap pesanan tanpa outlier. [Klik Di Sini](#9-rata-rata-profit-setelah-diskon-per-pesanan)
10. **Analisis RFM:** Menentukan segmentasi pelanggan berdasarkan Recency, Frequency, dan Monetary. [Klik Di Sini](#10-analisis-rfm)
11. **Distribusi Penjualan per Segmen Pelanggan:** Memberikan gambaran distribusi pendapatan penjualan di berbagai segmen pelanggan. [Klik Di Sini](#11-distribusi-penjualan-per-segmen-pelanggan)

# Tentang Data

## Data Penjualan Superstore: Deskripsi Kolom

| Nama Kolom      | Deskripsi                                                                   |
|-----------------|-----------------------------------------------------------------------------|
| order_id        | Identifikasi unik untuk setiap pesanan                                      |
| order_date      | Tanggal pesanan dibuat                                                      |
| ship_date       | Tanggal pesanan dikirimkan                                                  |
| ship_mode       | Metode pengiriman (mis. Standard Class, Second Class, Same Day)             |
| customer_name   | Nama pelanggan yang membuat pesanan                                         |
| segment         | Segmen pelanggan (mis. Consumer, Corporate, Home Office)                    |
| state           | Negara bagian atau provinsi tempat pelanggan berada                         |
| country         | Negara tempat pelanggan berada                                              |
| market          | Wilayah pasar (mis. APAC, EMEA, EU)                                         |
| region          | Wilayah spesifik dalam pasar (mis. North, South, Oceania)                   |
| product_id      | Identifikasi unik untuk setiap produk                                       |
| category        | Kategori produk (mis. Office Supplies, Furniture, Technology)               |
| sub_category    | Sub-kategori produk (mis. Storage, Paper, Appliances)                       |
| product_name    | Nama produk                                                                 |
| sales           | Jumlah penjualan untuk pesanan tersebut                                     |
| quantity        | Jumlah produk yang dipesan                                                  |
| discount        | Diskon yang diterapkan pada pesanan                                         |
| profit          | Profit yang diperoleh dari pesanan                                          |
| shipping_cost   | Biaya pengiriman pesanan                                                    |
| order_priority  | Tingkat prioritas pesanan (mis. High, Medium, Low, Critical)                |
| year            | Tahun pesanan dibuat                                                        |

## 10 Sampel Data per Kolom

| order_id      | order_date | ship_date | ship_mode     | customer_name   | segment       | state          | country   | market | region     | product_id       | category       | sub_category | product_name                                | sales | quantity | discount | profit  | shipping_cost | order_priority | year |
|---------------|------------|-----------|---------------|-----------------|---------------|----------------|-----------|--------|------------|------------------|----------------|--------------|---------------------------------------------|-------|----------|----------|---------|---------------|----------------|------|
| AG-2011-2040  | 1/1/2011   | 1/6/2011  | Standard Class| Toby Braunhardt| Consumer      | Constantine    | Algeria   | Africa | Africa     | OFF-TEN-10000025 | Office Supplies| Storage      | Tenex Lockers, Blue                        | 408   | 2        | 0        | 106.14  | 35.46         | Medium         | 2011 |
| IN-2011-47883 | 1/1/2011   | 1/8/2011  | Standard Class| Joseph Holt     | Consumer      | New South Wales| Australia | APAC   | Oceania    | OFF-SU-10000618  | Office Supplies| Supplies     | Acme Trimmer, High Speed                   | 120   | 3        | 0.1      | 36.036  | 9.72          | Medium         | 2011 |
| HU-2011-1220  | 1/1/2011   | 1/5/2011  | Second Class  | Annie Thurman   | Consumer      | Budapest       | Hungary   | EMEA   | EMEA       | OFF-TEN-10001585 | Office Supplies| Storage      | Tenex Box, Single Width                    | 66    | 4        | 0        | 29.64   | 8.17          | High           | 2011 |
| IT-2011-3647632| 1/1/2011   | 1/5/2011  | Second Class  | Eugene Moren    | Home Office   | Stockholm      | Sweden    | EU     | North      | OFF-PA-10001492  | Office Supplies| Paper        | Enermax Note Cards, Premium                | 45    | 3        | 0.5      | -26.055 | 4.82          | High           | 2011 |
| IN-2011-47883 | 1/1/2011   | 1/8/2011  | Standard Class| Joseph Holt     | Consumer      | New South Wales| Australia | APAC   | Oceania    | FUR-FU-10003447  | Furniture      | Furnishings | Eldon Light Bulb, Duo Pack                 | 114   | 5        | 0.1      | 37.77   | 4.70          | Medium         | 2011 |
| IN-2011-47883 | 1/1/2011   | 1/8/2011  | Standard Class| Joseph Holt     | Consumer      | New South Wales| Australia | APAC   | Oceania    | OFF-PA-10001968  | Office Supplies| Paper        | Eaton Computer Printout Paper, 8.5 x 11  | 55    | 2        | 0.1      | 15.342  | 1.80          | Medium         | 2011 |
| CA-2011-1510  | 1/2/2011   | 1/6/2011  | Standard Class| Magdelene Morse | Consumer      | Ontario        | Canada    | Canada | Canada     | TEC-OKI-10002750 | Technology     | Machines     | Okidata Inkjet, Wireless                   | 314   | 1        | 0        | 3.12    | 24.10         | Medium         | 2011 |
| IN-2011-79397 | 1/3/2011   | 1/3/2011  | Same Day      | Kean Nguyen    | Corporate     | New South Wales| Australia | APAC   | Oceania    | OFF-AP-10000304  | Office Supplies| Appliances   | Hoover Microwave, White                    | 276   | 1        | 0.1      | 110.412 | 125.32        | Critical       | 2011 |
| ID-2011-80230  | 1/3/2011   | 1/9/2011  | Standard Class| Ken Lonsdale    | Consumer      | Auckland       | New Zealand| APAC   | Oceania    | TEC-CO-10004182  | Technology     | Copiers      | Hewlett Wireless Fax, Laser                | 912   | 4        | 0.4      | -319.464| 107.1         | Low            | 2011 |

# Import Library
```python
import pandas as pd
import seaborn as sns
import matplotlib.pyplot as plt
import numpy as np
import datetime as dt
from datetime import date
from scipy.stats import mode
```
```python
df = pd.read_excel('superstore_sales.xlsx')
```

# Pengecekan Kualitas Data
## Missing Values
```python
print(df.isnull().sum())
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/bb85f82c-569e-47e1-bec6-7e3159fbbef7)

---

## Tipe Data
```python
df.dtypes
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/87dd5ab8-d957-4a97-b7d5-705424223a08)

---

## Statistik Deskriptif
```python
print(df.describe())
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/f406bf32-79f7-4f51-9624-33d23a5a90ae)

---

## Pengecekan Duplikat
```python
duplicate_rows = df.duplicated()

print("Duplicate Rows(True):", duplicate_rows.sum())
print("Duplicate Rows(False):", (len(duplicate_rows) - duplicate_rows.sum()))
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/4fcba36b-7a8b-46ca-aa22-e8c69ec6628c)

---

## 1. Tren Penjualan dan Profit Tahunan
```python
yearly_sales = df.groupby('year')['sales'].sum()
ax = yearly_sales.plot(kind='bar',color='darkblue', xlabel='Year', ylabel='Total Sales', title='Year to Year Sales Trend')

for i, v in enumerate(yearly_sales):
    ax.text(i, v + 0.03 * v, '${:,.0f}'.format(v), ha='center', va='bottom')
ax.set_ylim(0, max(yearly_sales) * 1.1)
ax.set_xticklabels(yearly_sales.index, rotation=45, ha='right')
plt.show()
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/e9fd5412-05e8-444a-899c-f6275eb8940b)
```python
yearly_profit = df.groupby('year')['profit'].sum()
ax = yearly_profit.plot(kind='bar',color='green', xlabel='Year', ylabel='Total profit', title='Year to Year profit Trend')

for i, v in enumerate(yearly_profit):
    ax.text(i, v + 0.03 * v, '${:,.0f}'.format(v), ha='center', va='bottom')
ax.set_ylim(0, max(yearly_profit) * 1.1)
ax.set_xticklabels(yearly_profit.index, rotation=45, ha='right')
plt.show()
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/e120c3d5-8b31-4a47-ac97-16d2f324ce75)

---

## 2. Penjualan per Kategori Produk
```python
category_sales = df.groupby('category')['sales'].sum().sort_values(ascending=False)
ax = category_sales.plot(kind='bar',color='darkblue', xlabel='Product Category', ylabel='Total Sales', title='Sales by Product Category')

for i, v in enumerate(category_sales):
    ax.text(i, v + 0.03 * v, '${:,.0f}'.format(v), ha='center', va='bottom')

ax.set_ylim(0, max(category_sales) * 1.1)
ax.set_xticklabels(category_sales.index, rotation=45, ha='right')
plt.show()
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/069a38e0-13fe-41bb-86a6-386565b3b853)
```python
# fungsi untuk mempersingkat nilai 'product_name' yang panjang
def shorten_name(name, max_length=30):
    if len(name) > max_length:
        return name[:max_length] + '...'
    else:
        return name

# memfilter data untuk setiap kategori
technology_data = df[df['category'] == 'Technology']
furniture_data = df[df['category'] == 'Furniture']
office_supplies_data = df[df['category'] == 'Office Supplies']

# fungsi untuk mendapatkan 5 product_name teratas
def get_top_products(data):
    top_products = data.groupby('product_name')['sales'].sum().sort_values(ascending=False).head(5)
    top_products.index = top_products.index.map(shorten_name)
    return top_products

# Top 5 produk untuk setiap kategori
top_tech_products = get_top_products(technology_data)
top_furniture_products = get_top_products(furniture_data)
top_office_supplies_products = get_top_products(office_supplies_data)
```
```python
# membuat bar chart untuk setiap kategori
fig, axs = plt.subplots(3, 1, figsize=(12, 18))

# Technology
axs[0].barh(top_tech_products.index, top_tech_products.values, color='skyblue')
axs[0].set_title('Top 5 Product - Technology')
axs[0].set_xlabel('Total Sales (K)')
axs[0].set_ylabel('Product Name')
for i, v in enumerate(top_tech_products.values):
    axs[0].text(v + 0.01 * v, i, '${:,.0f}K'.format(v / 1000), color='blue', va='center')

# Furniture
axs[1].barh(top_furniture_products.index, top_furniture_products.values, color='lightgreen')
axs[1].set_title('Top 5 Product - Furniture')
axs[1].set_xlabel('Total Sales (K)')
axs[1].set_ylabel('Product Name')
for i, v in enumerate(top_furniture_products.values):
    axs[1].text(v + 0.01 * v, i, '${:,.0f}K'.format(v / 1000), color='green', va='center')

# Office Supplies
axs[2].barh(top_office_supplies_products.index, top_office_supplies_products.values, color='salmon')
axs[2].set_title('Top 5 Product - Office Supplies')
axs[2].set_xlabel('Total Sales (K)')
axs[2].set_ylabel('Product Name')
for i, v in enumerate(top_office_supplies_products.values):
    axs[2].text(v + 0.01 * v, i, '${:,.0f}K'.format(v / 1000), color='red', va='center')

# menambahkan padding di sudut kiri
plt.subplots_adjust(left=0.3, right=0.9, top=0.9, bottom=0.1)

plt.tight_layout()
plt.show()
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/49056a7c-3002-4690-b679-a37ec7d5d749)

---

## 3. Distribusi Metode Pengiriman
```python
sns.countplot(x='ship_mode', data=df, color='skyblue')
plt.title('Shipping Mode Distribution')

for p in plt.gca().patches:
    plt.gca().annotate('{:,.0f}'.format(p.get_height()), (p.get_x() + p.get_width() / 2., p.get_height()), 
                       ha='center', va='bottom', xytext=(0, 5), textcoords='offset points')

plt.ylim(0, max(df['ship_mode'].value_counts()) * 1.1)
plt.xlabel('Ship Mode')
plt.ylabel('Total Shipment')
plt.show()
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/0f2c2968-8173-4819-8777-ffa3790f34e7)

---

## 4. Pendapatan per Negara/Wilayah
```python
def format_thousands(x):
    return '${:.1f}K'.format(x / 1000)

top_10_countries_profit = df.groupby('country')['profit'].sum().sort_values(ascending=False).head(10)

ax = top_10_countries_profit.plot(kind='barh',color='green', xlabel='Total profit', ylabel='Country', title='Profit by Country (Top 10)')

for i, v in enumerate(top_10_countries_profit):
    ax.text(v + 0.02 * v, i, format_thousands(v), ha='left', va='center')

ax.set_xlim(0, max(top_10_countries_profit) * 1.15)

plt.show()
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/7cf17f24-3c05-43b4-a4f6-65cb2225c198)

---

## 5. Frekuensi Pembelian Pelanggan
```python
customer_frequency = df['customer_name'].value_counts()

plt.hist(customer_frequency, bins=30, color='skyblue', alpha=0.7)

# Median, Q1, Q3
median = np.percentile(customer_frequency, 50)
q1 = np.percentile(customer_frequency, 25)
q3 = np.percentile(customer_frequency, 75)

# mode_value adalah nilai yang paling sering muncul, mis: '68' | mode_count adalah berapa kali nilai tersebut muncul, mis: '68' muncul sebanyak 30 kali
mode_value = mode(customer_frequency)[0]
mode_count = mode(customer_frequency)[1]

# menambahkan garis untuk median, Q1, Q3
plt.axvline(x=median, color='red', linestyle='--', linewidth=1.5, label='Median: {:.0f}'.format(median))
plt.axvline(x=q1, color='green', linestyle='--', linewidth=1.5, label='Q1: {:.0f}'.format(q1))
plt.axvline(x=q3, color='orange', linestyle='--', linewidth=1.5, label='Q3: {:.0f}'.format(q3))

# menambahkan garis untuk mode
if mode_value >= plt.gca().get_xlim()[0] and mode_value <= plt.gca().get_xlim()[1]:
    plt.axvline(x=mode_value, color='purple', linestyle='--', linewidth=1.5, label='Mode: {:.0f} ({}x)'.format(mode_value, mode_count))
else:
    plt.text(mode_value, plt.gca().get_ylim()[1] * 0.6, 'Mode: {:.0f} ({} x)'.format(mode_value, mode_count), color='purple', ha='center', va='center')

plt.legend()

plt.xlabel('Purchase Frequency')
plt.ylabel('Total Customers')
plt.title('Customer Purchase Frequency')

plt.show()
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/ef9fcc39-689e-4095-86ef-95c402c563d3)

---

## 6. Distribusi Prioritas Pesanan
```python
# membuat Countplot
sns.countplot(x='order_priority', data=df, color='skyblue')

# menambahkan nilai numerik di atas bar
for p in plt.gca().patches:
    plt.gca().annotate('{:,.0f}'.format(p.get_height()), (p.get_x() + p.get_width() / 2., p.get_height()), 
                       ha='center', va='bottom', xytext=(0, 1), textcoords='offset points')

plt.title('Order Priority Distribution')
plt.xlabel('Order Priority')
plt.ylabel('Total Order')

plt.show()
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/4561de56-c09f-4a1c-a21f-e7ae8f0a8738)

---

## 7. Korelasi antara Diskon dan Profit
```python
# membuat scatter plot antara Discount dan profit
sns.scatterplot(x='discount', y='profit', data=df, color='skyblue', alpha=0.8)

# variabel yang menghitung koefisien korelasi antara discount dan profit
correlation_coefficient = df['discount'].corr(df['profit'])

# menambahkan koefisien korelasi ke dalam plot
plt.text(0.2, -2000, 'Correlation Coefficient: {:.2f}'.format(correlation_coefficient), fontsize=10, color='red')

plt.xlabel('Discount (%)')
plt.ylabel('Profit')
plt.title('Correlation between Discount and Profit')

plt.show()
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/6898a01f-67c7-486f-b894-d1bcd3e3cb57)

---

## 8. Profit Bulanan (Setelah Diskon)
```python
def format_thousands(x):
    return '{:.1f}K'.format(x / 1000)

df['order_date'] = pd.to_datetime(df['order_date'])

df['year'] = df['order_date'].dt.year
df['month'] = df['order_date'].dt.month

monthly_profit = df.groupby(['year', 'month'])['profit'].sum()

fig, axes = plt.subplots(2, 2, figsize=(15, 10))

# melakukan looping untuk setiap sumbu subplot dan tahun yang sesuai dari 2011 hingga 2014
for ax, year in zip(axes.flatten(), range(2011, 2015)):
    data = monthly_profit.loc[year]
    ax.plot(data.index, data.values, marker='o', linestyle='-', alpha=0.5)
    ax.set_title('Monthly Profit by Year {}'.format(year))
    ax.set_xlabel('Months')
    ax.set_ylabel('Profit')
    
    for i, v in zip(data.index, data.values):
        ax.text(i, v * 1.02, format_thousands(v), ha='center', va='bottom')

    ax.set_ylim(0, max(data.values) * 1.08)

# menambahkan legenda
axes[0, 0].legend(['Profit'], loc='upper left')
axes[0, 1].legend(['Profit'], loc='upper left')
axes[1, 0].legend(['Profit'], loc='upper left')
axes[1, 1].legend(['Profit'], loc='upper left')

plt.tight_layout()
plt.show()
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/423eb2eb-4f7e-4136-a12c-b6eb7eca0257)

---

## 9. Rata-rata Profit (Setelah Diskon) per Pesanan
```python
# menghitung statistik deskriptif profit per pesanan
order_income_stats = df.groupby('order_id')['profit'].sum().describe()

# menghitung IQR
Q1 = order_income_stats['25%']
Q3 = order_income_stats['75%']
IQR = Q3 - Q1

# mendefinisikan batas atas dan bawah tanpa outlier
lower_bound = Q1 - 1.5 * IQR
upper_bound = Q3 + 1.5 * IQR
avg_profit_order_no_outliers = df.groupby('order_id')['profit'].sum().loc[(df.groupby('order_id')['profit'].sum() >= lower_bound) & (df.groupby('order_id')['profit'].sum() <= upper_bound)]
avg_profit_order_no_outliers.describe()
```

### Output :

| Statistic | Value        |
|-----------|--------------|
| Count     | 20500.000000 |
| Mean      | 32.443220    |
| Std       | 62.547835    |
| Min       | -133.548000  |
| 25%       | 1.500000     |
| 50%       | 17.252400    |
| 75%       | 59.400000    |
| Max       | 222.740000   |
```python
plt.figure(figsize=(10, 6))
avg_profit_order_no_outliers.hist(bins=30, color='skyblue', edgecolor='black')
plt.xlabel('Profit per Order')
plt.ylabel('Total Order')
plt.title('Profit per Order Distribution without Outliers')

plt.text(0.5, 0.95, f"Count: {avg_profit_order_no_outliers.count()}", transform=plt.gca().transAxes)
plt.text(0.5, 0.9, f"Mean: {avg_profit_order_no_outliers.mean():.2f}", transform=plt.gca().transAxes)
plt.text(0.5, 0.85, f"Std: {avg_profit_order_no_outliers.std():.2f}", transform=plt.gca().transAxes)
plt.text(0.5, 0.8, f"Min: {avg_profit_order_no_outliers.min():.2f}", transform=plt.gca().transAxes)
plt.text(0.5, 0.75, f"25%: {avg_profit_order_no_outliers.quantile(0.25):.2f}", transform=plt.gca().transAxes)
plt.text(0.5, 0.7, f"50%: {avg_profit_order_no_outliers.quantile(0.50):.2f}", transform=plt.gca().transAxes)
plt.text(0.5, 0.65, f"75%: {avg_profit_order_no_outliers.quantile(0.75):.2f}", transform=plt.gca().transAxes)
plt.text(0.5, 0.6, f"Max: {avg_profit_order_no_outliers.max():.2f}", transform=plt.gca().transAxes)

plt.grid(False)
plt.show()
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/c1ec955b-6050-4d34-8332-ab78932036c0)

---

## 10. Analisis RFM
```python
latest_date = df['order_date'].max()

# menghitung nilai Recency, Frequency, dan Monetary
rfm_table = df.groupby('customer_name').agg({
    'order_date': lambda x: (latest_date - x.max()).days,
    'order_id': 'count',
    'profit': 'sum'
})

# mengganti nama kolom menjadi Recency, Frequency, dan Monetary
rfm_table.rename(columns={
    'order_date': 'Recency',
    'order_id': 'Frequency',
    'profit': 'Monetary'
}, inplace=True)

# melakukan normalisasi nilai RFM
rfm_table['Recency'] = (rfm_table['Recency'] - rfm_table['Recency'].min()) / (rfm_table['Recency'].max() - rfm_table['Recency'].min())
rfm_table['Frequency'] = (rfm_table['Frequency'] - rfm_table['Frequency'].min()) / (rfm_table['Frequency'].max() - rfm_table['Frequency'].min())
rfm_table['Monetary'] = (rfm_table['Monetary'] - rfm_table['Monetary'].min()) / (rfm_table['Monetary'].max() - rfm_table['Monetary'].min())

# memberikan skor RFM
rfm_table['R_Score'] = pd.qcut(rfm_table['Recency'], 4, ['1', '2', '3', '4'])
rfm_table['F_Score'] = pd.qcut(rfm_table['Frequency'], 4, ['4', '3', '2', '1'])
rfm_table['M_Score'] = pd.qcut(rfm_table['Monetary'], 4, ['4', '3', '2', '1'])

# menggabungkan skor menjadi satu kolom
rfm_table['RFM_Score'] = rfm_table['R_Score'].astype(str) + rfm_table['F_Score'].astype(str) + rfm_table['M_Score'].astype(str)
rfm_table.sample(5)
```

### Output :

| customer_name   | Recency  | Frequency | Monetary | R_Score | F_Score | M_Score | RFM_Score |
|-----------------|----------|-----------|----------|---------|---------|---------|-----------|
| Tamara Manning | 0.149533 | 0.329114  | 0.545024 | 4       | 4       | 2       | 442       |
| Susan Gilcrest | 0.037383 | 0.367089  | 0.451475 | 2       | 3       | 4       | 234       |
| Andy Reiter    | 0.014019 | 0.075949  | 0.626710 | 1       | 4       | 1       | 141       |
| Brian Moss     | 0.077103 | 0.620253  | 0.710812 | 3       | 1       | 1       | 311       |
| Joseph Airdo   | 0.000000 | 0.594937  | 0.471780 | 1       | 1       | 4       | 114       |
```python
plt.figure(figsize=(14, 18))

# membuat scatter plot untuk Recency dan Frequency
plt.subplot(3, 1, 1)
sns.scatterplot(x='Recency', y='Frequency', size='Monetary', sizes=(20, 200), hue='Monetary', data=rfm_table, palette='viridis', legend=False)
plt.title('Recency vs Frequency')
plt.xlabel('Recency')
plt.ylabel('Frequency')

# membuat scatter plot untuk Frequency dan Monetary
plt.subplot(3, 1, 2)
sns.scatterplot(x='Frequency', y='Monetary', size='Recency', sizes=(20, 200), hue='Recency', data=rfm_table, palette='viridis', legend=False)
plt.title('Frequency vs Monetary')
plt.xlabel('Frequency')
plt.ylabel('Monetary')

# membuat scatter plot untuk Recency dan Monetary
plt.subplot(3, 1, 3)
sns.scatterplot(x='Recency', y='Monetary', size='Frequency', sizes=(20, 200), hue='Frequency', data=rfm_table, palette='viridis', legend=False)
plt.title('Recency vs Monetary')
plt.xlabel('Recency')
plt.ylabel('Monetary')

plt.tight_layout()
plt.show()
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/8384fad1-4831-49f1-ab33-5c560dc6ca6d)

---

## 11. Distribusi Penjualan per Segmen Pelanggan
Bagian ini memberikan gambaran distribusi pendapatan penjualan di berbagai segmen pelanggan.
```python
sales_by_segment = df.groupby('segment')['sales'].sum().reset_index()
sales_numeric = sales_by_segment['sales'].copy()
# memformat tanpa notasi ilmiah atau koma
sales_by_segment['sales'] = sales_by_segment['sales'].apply(lambda x: f'${x:,.0f}')
print(sales_by_segment)
```

### Output :

| segment      | sales        |
|--------------|--------------|
| Consumer     | $6,507,949   |
| Corporate    | $3,824,698   |
| Home Office  | $2,309,855   |
```python
segments = sales_by_segment['segment']

# warna untuk setiap segmen
colors = ['green', 'skyblue', 'orange']
plt.figure(figsize=(10, 7))

# fungsi untuk menampilkan persentase dan nilai absolut
def autopct_format(values):
    def my_format(pct):
        total = sum(values)
        val = int(round(pct*total/100.0))
        return f'{pct:.1f}%\n(${val:,.0f})'
    return my_format

plt.pie(sales_numeric, labels=segments, autopct=autopct_format(sales_numeric), startangle=140, colors=colors, shadow=True, explode=(0.05, 0, 0))
plt.title('Sales by Segment', fontsize=16)
plt.legend(segments, title="Segments", loc="center left", bbox_to_anchor=(1, 0, 0.5, 1))
plt.axis('equal')

plt.show()
```

![image](https://github.com/Ruzsel/Superstore_Analysis/assets/150054552/b4ee7cf7-9aeb-4ff3-a601-5444b7a3692e)

---

# Temuan dan Solusi Bisnis

## 1. Tren Penjualan dan Profit Tahunan

Data Penjualan:
- 2011: $2.259.451
- 2012: $2.677.439
- 2013: $3.405.746
- 2014: $4.299.866

Data Profit:
- 2011: $248.941
- 2012: $307.415
- 2013: $408.513
- 2014: $504.166

### CAGR (Compound Annual Growth Rate) Penjualan
- CAGR = (Vf / Vi)^(1/n) - 1
- CAGR = (4.299.866 / 2.259.451)^(1/3) - 1
- CAGR ≈ (1,902)^(1/3) - 1
- CAGR ≈ 1,227 - 1
- CAGR ≈ 0,227
- CAGR ≈ 22,7%

### CAGR (Compound Annual Growth Rate) Profit
- CAGR = (Vf / Vi)^(1/n) - 1
- CAGR = (504.166 / 248.941)^(1/3) - 1
- CAGR ≈ (2,025)^(1/3) - 1
- CAGR ≈ 1,259 - 1
- CAGR ≈ 0,259
- CAGR ≈ 25,9%

### Ringkasan
- CAGR Penjualan (2011-2014): 22,7%
- CAGR Profit (2011-2014): 25,9%

## Solusi Bisnis
Analisis CAGR untuk penjualan dan profit dari 2011 hingga 2014 menunjukkan tingkat pertumbuhan yang signifikan. Berikut beberapa solusi bisnis berdasarkan tren tersebut:
- **Strategi Pertumbuhan Penjualan:** Memanfaatkan tren pertumbuhan penjualan yang kuat dengan memperluas jangkauan pasar melalui kampanye pemasaran yang tertarget, mengeksplorasi segmen pelanggan baru, dan meningkatkan penawaran produk untuk memenuhi kebutuhan konsumen yang terus berkembang.
- **Manajemen Risiko:** Meski CAGR menunjukkan pertumbuhan positif, penting untuk menilai dan memitigasi risiko yang menyertainya. Melakukan analisis pasar secara menyeluruh, memantau tren industri, dan menyusun rencana kontingensi untuk menghadapi potensi tantangan seperti kejenuhan pasar, tekanan kompetitif, atau perlambatan ekonomi.

---

## 2. Penjualan per Kategori Produk

Penjualan per Kategori Produk:
- Technology: $4.744.557
- Furniture: $4.110.874
- Office Supplies: $3.787.070

TOP 5 Produk - Technology:
1. Canon ImageCLASS 2200 = $62K
2. Nokia Smart Phone = $72K
3. Motorola Smartphone = $73K
4. Cisco Smart Phone = $76K
5. Apple Smart Phone = $87K

TOP 5 Produk - Furniture:
1. Novimex Executive Leather = $41K
2. SAFCO Executive Leather = $42K
3. Harbour Creations Executive = $50K
4. Office Star Executive = $51K
5. Hon Executive Leather = $58K

TOP 5 Produk - Office Supplies:
1. Smead Lockers = $29K
2. Rogers File Cart = $29K
3. Hoover Stove, Red = $32K
4. Hoover Stove, White = $33K
5. Eldon File Cart = $34K

## Solusi Bisnis

### Meningkatkan Pemasaran untuk Produk Teknologi Berdemand Tinggi
- **Mengintensifkan Upaya Iklan:** Meluncurkan kampanye pemasaran tertarget yang menekankan fitur dan keunggulan terkini dari produk teknologi terlaris seperti smartphone Apple, Cisco, dan Motorola.
- **Penawaran Bundling:** Membuat paket bundling menarik yang menggabungkan smartphone populer dengan aksesori (mis. headphone, case) untuk meningkatkan nilai transaksi rata-rata.
- **Memanfaatkan Media Sosial dan Influencer:** Menggunakan platform media sosial dan influencer teknologi untuk mempromosikan produk-produk ini, memanfaatkan basis konsumen yang melek teknologi.

### Memperluas Ragam Produk di Kategori Furniture dan Office Supplies
- **Diversifikasi Produk:** Memperkenalkan produk baru dalam kategori ini untuk memenuhi kebutuhan pelanggan yang beragam. Untuk Furniture, mempertimbangkan penambahan kursi ergonomis dan standing desk. Untuk Office Supplies, mengeksplorasi alat organisasi inovatif dan produk ramah lingkungan.
- **Umpan Balik Pelanggan:** Melakukan survei dan focus group untuk memahami preferensi pelanggan dan kesenjangan dalam ragam produk saat ini, lalu menggunakannya sebagai dasar pengembangan produk baru.
- **Promosi Musiman:** Menjalankan promosi dan diskon musiman pada item berperforma tinggi seperti kursi executive dan file cart untuk mendorong penjualan di periode belanja puncak.

### Mengoptimalkan Manajemen Inventaris dan Rantai Pasokan
- **Manajemen Inventaris Berbasis Data:** Menggunakan data penjualan untuk memprediksi permintaan secara akurat dan mengoptimalkan tingkat inventaris, memastikan produk populer selalu tersedia.
- **Hubungan dengan Pemasok:** Memperkuat hubungan dengan pemasok utama untuk memastikan pengisian stok produk berdemand tinggi tepat waktu dan menegosiasikan syarat yang lebih baik untuk pembelian dalam jumlah besar.
- **Efisiensi Rantai Pasokan:** Mengimplementasikan teknologi rantai pasokan terkini untuk memperlancar logistik, mengurangi lead time, serta meminimalkan kehabisan stok atau kelebihan stok.

---

## 3. Distribusi Metode Pengiriman

Distribusi Metode Pengiriman:
- Standard Class: 30.775 pengiriman
- Second Class: 10.309 pengiriman
- Same Day: 2.701 pengiriman
- First Class: 7.505 pengiriman

## Insight
- **Dominasi Standard Class:** Sebagian besar pengiriman (30.775) menggunakan Standard Class, mengindikasikan preferensi terhadap pengiriman yang ekonomis.
- **Penggunaan Same Day yang Terbatas:** Same Day shipping adalah metode yang paling jarang digunakan dengan hanya 2.701 pengiriman, menunjukkan permintaan yang lebih rendah atau biaya yang lebih tinggi.
- **Preferensi Sedang untuk Pengiriman Premium:** First Class dan Second Class memiliki penggunaan yang moderat (masing-masing 7.505 dan 10.309 pengiriman), mengindikasikan adanya sebagian pelanggan yang bersedia membayar lebih untuk pengiriman lebih cepat.

## Solusi Bisnis

### Mengoptimalkan Pengiriman Standard Class
- **Menegosiasikan Kontrak Massal:** Mengurangi biaya melalui kontrak pengiriman massal dengan penyedia logistik.
- **Meningkatkan Proses:** Meningkatkan efisiensi gudang dan pemrosesan pesanan untuk mempercepat pengiriman Standard Class.
- **Komunikasi yang Jelas:** Menetapkan ekspektasi yang jelas mengenai waktu pengiriman Standard Class untuk menjaga kepuasan pelanggan.

### Mempromosikan Pilihan Pengiriman Lebih Cepat
- **Insentif:** Menawarkan diskon atau promosi untuk mendorong pelanggan beralih ke opsi pengiriman yang lebih cepat.
- **Integrasi Loyalitas:** Menyertakan manfaat pengiriman premium dalam program loyalitas pelanggan.
- **Menonjolkan Keunggulan:** Menonjolkan keunggulan pengiriman lebih cepat untuk menarik lebih banyak pelanggan.

### Memperluas dan Mempromosikan Same Day Shipping
- **Memperluas Jangkauan:** Meningkatkan ketersediaan Same Day shipping di lebih banyak wilayah, terutama area perkotaan.
- **Kampanye Tertarget:** Menggunakan pemasaran untuk mempromosikan kemudahan Same Day shipping bagi kebutuhan mendesak.
- **Mengoptimalkan Biaya:** Bermitra dengan layanan pengiriman lokal dan meningkatkan perencanaan rute untuk mengelola biaya secara efektif.

---

## 4. Pendapatan per Negara/Wilayah

Temuan Pendapatan per Negara/Wilayah:
- United States: $286.397
- China: $150.683
- India: $129.072
- United Kingdom: $111.900
- France: $109.029
- Germany: $107.323
- Australia: $105.485
- Mexico: $102.818
- Spain: $54.390
- El Salvador: $42.023

## Insight
- **Distribusi Pendapatan:** Amerika Serikat memimpin dalam hal pendapatan, diikuti China dan India, mencerminkan kekuatan ekonomi dan ukuran pasar mereka.
- **Kehadiran di Eropa:** Negara-negara Eropa seperti Inggris, Prancis, Jerman, dan Spanyol juga berkontribusi signifikan terhadap pendapatan, mengindikasikan kehadiran pasar yang kuat di kawasan tersebut.
- **Pasar Berkembang:** Negara-negara seperti India, China, dan Meksiko mewakili pasar berkembang dengan kontribusi pendapatan yang substansial, menyoroti peluang untuk pertumbuhan dan ekspansi lebih lanjut.

## Solusi Bisnis

### Penetrasi dan Ekspansi Pasar
- **Investasi Strategis:** Mengalokasikan sumber daya untuk menembus dan memperluas pasar berpendapatan tinggi seperti Amerika Serikat dan Eropa.
- **Strategi Terlokalisasi:** Mengembangkan strategi pemasaran dan produk yang terlokalisasi, disesuaikan dengan preferensi dan tren di setiap negara atau wilayah.
- **Kemitraan dan Aliansi:** Membentuk kemitraan atau aliansi dengan bisnis atau distributor lokal untuk meningkatkan penetrasi pasar dan visibilitas merek.

### Fokus pada Pasar Berkembang
- **Riset Pasar:** Melakukan riset pasar mendalam untuk memahami dinamika dan peluang di pasar berkembang seperti India, China, dan Meksiko.
- **Adaptasi:** Mengadaptasi produk, penetapan harga, dan strategi distribusi agar sesuai dengan kebutuhan dan preferensi unik konsumen di pasar-pasar ini.
- **Investasi Infrastruktur:** Menginvestasikan dana dalam membangun jaringan distribusi dan infrastruktur untuk mendukung operasional dan pertumbuhan penjualan di pasar berkembang.

---

## 5. Frekuensi Pembelian Pelanggan

Temuan Frekuensi Pembelian Pelanggan:
- Median: 64
- Q1 (Kuartil Pertama): 55
- Q3 (Kuartil Ketiga): 74
- Mode: 68

## Insight
- **Tendensi Sentral:** Median frekuensi pembelian sebesar 64 menunjukkan bahwa separuh pelanggan melakukan pembelian lebih sering dari nilai ini, sementara separuh lainnya lebih jarang.
- **Variabilitas:** Rentang interkuartil (Q3-Q1) sebesar 19 menunjukkan sebaran nilai frekuensi pembelian antara persentil ke-25 dan ke-75, mengindikasikan variabilitas yang moderat.
- **Frekuensi Umum:** Mode sebesar 68 menunjukkan bahwa frekuensi pembelian yang paling umum di antara pelanggan adalah 68, mengimplikasikan konsentrasi pelanggan di sekitar nilai ini.

## Solusi Bisnis

### Kampanye Pemasaran yang Dipersonalisasi
- **Segmentasi:** Melakukan segmentasi pelanggan berdasarkan frekuensi pembelian mereka untuk menyesuaikan kampanye pemasaran dengan kebiasaan belanja masing-masing.
- **Penawaran Tertarget:** Menawarkan promosi atau diskon khusus untuk mendorong pelanggan yang frekuensi pembeliannya di bawah median agar meningkatkan frekuensi tersebut.
- **Strategi Retensi:** Mengimplementasikan strategi retensi pelanggan untuk mendorong pembeli frequent mempertahankan kebiasaan pembelian mereka dan mencegah churn.

### Umpan Balik dan Keterlibatan
- **Umpan Balik Pelanggan:** Meminta umpan balik dari pelanggan untuk memahami faktor-faktor yang memengaruhi frekuensi pembelian dan preferensi mereka.
- **Inisiatif Keterlibatan:** Melibatkan pelanggan melalui program loyalitas, konten interaktif, atau aktivitas membangun komunitas untuk menumbuhkan loyalitas merek dan mendorong pembelian berulang.
- **Pemantauan Berkelanjutan:** Memantau perilaku pembelian pelanggan secara berkelanjutan dan mengadaptasi strategi sesuai kebutuhan untuk menjaga tingkat frekuensi pembelian yang optimal.

---

## 6. Distribusi Prioritas Pesanan

Temuan Distribusi Prioritas Pesanan:
- Medium: 29.433
- High: 15.501
- Critical: 3.932
- Low: 2.424

## Insight
- **Tingkat Prioritas:** Pesanan tersebar di berbagai tingkat prioritas, mulai dari Low hingga Critical, mencerminkan tingkat urgensi dan kepentingan yang bervariasi.
- **Dominasi Prioritas Medium:** Pesanan prioritas Medium merupakan mayoritas, menunjukkan bahwa sebagian besar pesanan membutuhkan penanganan segera namun belum bersifat mendesak.
- **Pesanan Critical:** Meski jumlah pesanan Critical paling rendah, keberadaannya menegaskan pentingnya menangani kebutuhan pelanggan yang mendesak dengan cepat.

## Solusi Bisnis

### Optimalisasi Alur Kerja
- **Alur Kerja Berbasis Prioritas:** Mengimplementasikan sistem alur kerja berbasis prioritas untuk memperlancar pemrosesan pesanan, memastikan pesanan prioritas tinggi ditangani lebih cepat sekaligus menjaga efisiensi untuk pesanan prioritas rendah.
- **Otomatisasi:** Memanfaatkan teknologi otomatisasi untuk memprioritaskan dan mengarahkan pesanan berdasarkan tingkat prioritasnya, mengurangi waktu pemrosesan manual dan meningkatkan akurasi.

### Komunikasi dengan Pelanggan
- **Transparansi:** Mengomunikasikan status prioritas pesanan secara jelas kepada pelanggan, menetapkan ekspektasi realistis untuk waktu pengiriman dan respons berdasarkan prioritas pesanan.
- **Notifikasi Proaktif:** Mengimplementasikan sistem notifikasi proaktif untuk memperbarui pelanggan mengenai status pesanan mereka, terutama untuk pesanan Critical, guna memberikan rasa aman dan menjaga kepuasan pelanggan.

---

## 7. Korelasi antara Diskon dan Profit

Korelasi antara Diskon dan Profit:
- Koefisien Korelasi: -0,32

## Insight
- **Korelasi Negatif:** Koefisien korelasi -0,32 mengindikasikan korelasi negatif antara diskon dan profit. Artinya, semakin besar diskon yang diberikan, profit cenderung semakin menurun, dan sebaliknya.
- **Hubungan Berlawanan Arah:** Korelasi negatif ini mengimplikasikan hubungan terbalik antara diskon dan profit, sehingga menawarkan diskon yang lebih tinggi dapat mengakibatkan profit yang lebih rendah.

## Solusi Bisnis

### Pemberian Diskon yang Tertarget
- **Segmentasi:** Melakukan segmentasi pelanggan berdasarkan perilaku pembelian, preferensi, dan sensitivitas harga untuk menawarkan diskon tertarget kepada pelanggan bernilai tinggi, sekaligus meminimalkan diskon untuk segmen bermargin rendah.
- **Bundling Promosi:** Menawarkan diskon sebagai bagian dari bundling promosi atau program loyalitas untuk mendorong pembelian tambahan dan memitigasi dampak diskon individual terhadap margin profit.

---

## 8. Profit Bulanan (Setelah Diskon)

Tahun 2011:
- Januari: $8,3K
- Juni: $23,4K
- Juli: $5,6K
- September: $35,8K
- Desember: $40,6K

Tahun 2012:
- Januari: $10,4K
- Juni: $34,4K
- Juli: $15,6K
- Agustus: $43,6K
- Desember: $33K

Tahun 2013:
- Januari: $26,8K
- Juni: $45,5K
- Juli: $28,9K
- Desember: $50,2K

Tahun 2014:
- Januari: $28K
- Juni: $43,8K
- Juli: $28K
- September: $68K
- Desember: $46,9K

## Insight
- **Variasi Musiman:** Profit berfluktuasi sepanjang tahun, dengan bulan-bulan tertentu mengalami puncak lebih tinggi dan yang lain lebih rendah di semua tahun.
- **Analisis Tren:** Secara keseluruhan, terdapat tren kenaikan profit dari tahun ke tahun, meski ada fluktuasi di bulan-bulan tertentu.
- **Pola Tahunan:** Setiap tahun menunjukkan pola fluktuasi profit yang serupa, dengan beberapa bulan yang secara konsisten memberikan kinerja lebih baik dari yang lain.

## Solusi Bisnis

### Promosi Musiman
- **Kampanye Tertarget:** Meluncurkan promosi musiman dan kampanye pemasaran di bulan-bulan puncak untuk memanfaatkan peningkatan belanja konsumen dan memaksimalkan profitabilitas.
- **Manajemen Inventaris:** Mengantisipasi fluktuasi permintaan dan menyesuaikan tingkat inventaris untuk memastikan stok yang cukup di periode puncak, sekaligus meminimalkan kelebihan inventaris di bulan-bulan lebih sepi.

### Optimalisasi Biaya
- **Tinjauan Pengeluaran:** Melakukan tinjauan komprehensif terhadap pengeluaran dan mengidentifikasi peluang optimalisasi biaya untuk menjaga profitabilitas di bulan-bulan lebih sepi.
- **Negosiasi dengan Pemasok:** Menegosiasikan syarat yang menguntungkan dengan pemasok untuk mengurangi biaya pengadaan dan meningkatkan margin, terutama di periode profitabilitas yang lebih rendah.

---

## 9. Rata-rata Profit (Setelah Diskon) per Pesanan
- Jumlah: 20.500 pesanan
- Rata-rata: $32 (dibulatkan)
- Standar Deviasi: $63 (dibulatkan)
- Minimum: -$134
- Persentil ke-25 (Q1): $2
- Median (Persentil ke-50): $17
- Persentil ke-75 (Q3): $59
- Maksimum: $223

## Insight
- **Rata-rata Profit:** Rata-rata profit per pesanan setelah diskon adalah sekitar $32.
- **Variabilitas:** Standar deviasi sekitar $63 menunjukkan variasi yang cukup besar pada nilai profit di sekitar rata-rata.
- **Distribusi:** Data berdistribusi positif skewed, dengan outlier di ujung atas spektrum profit.

## Solusi Bisnis

### Analisis Profitabilitas
- **Analisis Segmen:** Memanfaatkan analitik data untuk mengidentifikasi segmen pelanggan atau kategori produk berprofit tinggi dan mengalokasikan sumber daya sesuai kebutuhan.
- **Optimalisasi Bauran Produk:** Menganalisis data profitabilitas untuk mengoptimalkan bauran produk, memfokuskan diri pada produk bermargin tinggi guna meningkatkan profitabilitas secara keseluruhan.

### Manajemen Biaya
- **Strategi Pengurangan Biaya:** Mengimplementasikan strategi pengurangan biaya berdasarkan insight berbasis data, seperti merampingkan operasional dan menegosiasikan kontrak pemasok untuk meningkatkan margin profit.

---

## 10. Distribusi Penjualan per Segmen Pelanggan
- Consumer: $6.507.949
- Corporate: $3.824.698
- Home Office: $2.309.855

## Insight
- **Dominasi Segmen Consumer:** Segmen Consumer menyumbang volume penjualan tertinggi, mengindikasikan porsi pendapatan yang signifikan berasal dari pelanggan individu.
- **Kontribusi Segmen Corporate:** Segmen Corporate berkontribusi secara substansial terhadap penjualan, menunjukkan kinerja penjualan business-to-business yang kuat.
- **Segmen Home Office:** Meski berkontribusi paling kecil terhadap penjualan, segmen Home Office tetap mewakili porsi pendapatan yang cukup berarti, menegaskan pentingnya melayani pelanggan small office dan home office.

## Solusi Bisnis

### Strategi Pemasaran Tertarget
- **Kampanye Spesifik per Segmen:** Mengembangkan kampanye pemasaran tertarget yang disesuaikan untuk setiap segmen pelanggan guna mengomunikasikan value proposition produk secara efektif dan meningkatkan kinerja penjualan.
- **Personalisasi:** Memanfaatkan data pelanggan untuk mempersonalisasi pesan dan penawaran pemasaran bagi setiap segmen, meningkatkan relevansi dan keterlibatan.

### Optimalisasi Ragam Produk
- **Produk Spesifik per Segmen:** Mengoptimalkan ragam produk untuk memenuhi kebutuhan dan preferensi unik setiap segmen pelanggan, memastikan tersedianya penawaran yang beragam dan disesuaikan dengan demografi pelanggan yang berbeda.
- **Bundling Produk:** Membuat paket produk bundling yang disesuaikan dengan preferensi tiap segmen untuk mendorong nilai pesanan yang lebih tinggi dan meningkatkan kepuasan pelanggan.

---
