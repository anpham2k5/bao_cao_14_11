# Báo cáo tiến độ nghiên cứu ngày 14/11/2026
## A. Công việc đã làm
- Đo so sánh 2 mạch và tìm dải đo đẹp nhất
- Đo dải đo đấy xét độ tuyến tính của 2 mạch
## B. Khó Khăn
## C. Báo cáo chi tiết 
### 1. Code chi tiết
https://github.com/anpham2k5/bao_cao_14_11/tree/master/STM32_ADC_Touch/src
### 2. Đo so sánh 2 mạch và tìm dải đo đẹp nhất
- Tất cả lần đo đều rút sạc máy tính, rút những dây không dùng và đã khắc phục lỗi GND
- Cùng 1 lớp điện môi đàn hồi
- Hình ảnh lúc đo

| | Mạch 2 | Mạch 3 |
| :---: | :---: | :---: |
| 4N | ![](image/mach2_400.jpg) | ![](image/mach3_400.jpg) |
| 6N | ![](image/mach2_600.jpg) | ![](image/mach3_600.jpg) |
| 8N | ![](image/mach2_800.jpg) | ![](image/mach3_800.jpg) |
| 10N | ![](image/mach2_1000.jpg) | ![](image/mach3_1000.jpg) |
| 12N | ![](image/mach2_1200.jpg) | ![](image/mach3_1200.jpg) |
| 16N | ![](image/mach2_1600.jpg) | ![](image/mach3_1600.jpg) |

- Đồ thị so sánh 2 mạch theo các mức lực

| Mạch 2 | Mạch 3 |
| :---: | :---: |
| ![](image/luc_mach2.jpg) | ![](image/luc_mach3.jpg) |

#### Nhận xét: 
- Từ đồ thị ta thấy dải đo đẹp nhất là từ 4N-12N

### 3. Đo 2 mạch với dải đo từ 4N-12N
- Lúc đo khác miếng điện môi đàn hồi
- Đồ thị 2 mạch 

| Mạch 2 | Mạch 3 |
| :---: | :---: |
| ![](image/luc_mach2.jpg) | ![](image/tuyentinh_mach3.jpg) |

#### Nhận xét:
- Ở mạch 1 với nhiều môi trường và nhiều máy khác nhau thì giá trị đo từ mạch luôn cho ra một kết quả thiếu ổn định

### 4. Đo lệch về phía tụ 1, 2 một ít

- Đồ thị
<div align="center">

![](image/dolech.jpg)

</div>

### 5. Xem lực đủ để gắp trứng 
- Hình ảnh lúc kiểm tra
<div align="center">

![](image/trung.jpg)

</div>

#### Giá trị ADC của 2 mạch khi kiểm tra với trứng

<table>
<tr>
<th align="center">Mạch 2</th>
<th align="center">Mạch 3</th>
</tr>
<tr>
<td valign="top">

<pre><code class="language-cpp">5.41    8.41    5.65    3.62;
5.59    9.36    6.20    3.74;
5.78    10.11   6.56    3.83;
6.03    10.26   6.64    4.00;
6.11    10.41   6.59    4.00;
6.25    10.71   6.69    3.96;
6.38    10.93   6.80    4.06;
6.61    11.16   6.96    4.25;
6.68    11.49   7.15    4.32;
6.77    11.74   7.21    4.30;
6.93    11.98   7.27    4.24;
6.92    12.08   7.23    4.24;
7.09    12.46   7.34    4.25;
7.27    12.49   7.36    4.33;
7.30    12.44   7.31    4.39;</code></pre>

</td>
<td valign="top">

<pre><code class="language-cpp">9.06    11.18   1.39    0.70;
9.85    11.45   1.41    0.92;
10.23   11.72   1.69    1.33;
11.39   12.42   1.89    1.79;
11.73   11.91   1.85    1.99;
12.13   11.76   2.01    2.24;
12.41   11.53   1.98    2.34;
12.77   11.45   2.13    2.57;
13.25   11.39   2.20    2.93;
13.81   11.44   2.31    3.32;
14.19   11.47   2.38    3.32;
14.65   11.50   2.40    3.46;
15.14   11.58   2.46    3.76;
15.64   11.57   2.63    4.05;
16.10   11.45   2.63    4.29;
</code></pre>

</td>
</tr>
</table>

#### Nhận xét:
- Lực đủ để giữ trứng khoảng từ 6N-10N
