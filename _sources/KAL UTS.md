# Eliminasi Gauss & Gauss-Jordan (SPL 5 Variabel)

## 1. Sistem Persamaan Linear

\[
\begin{cases}
2x+y+z+w+v=10 \\
x+3y+z+w+v=12 \\
x+y+4z+w+v=14 \\
x+y+z+5w+v=16 \\
x+y+z+w+6v=18
\end{cases}
\]

---

## 2. Matriks Augmented Awal

\[
\left[
\begin{array}{ccccc|c}
2 & 1 & 1 & 1 & 1 & 10 \\
1 & 3 & 1 & 1 & 1 & 12 \\
1 & 1 & 4 & 1 & 1 & 14 \\
1 & 1 & 1 & 5 & 1 & 16 \\
1 & 1 & 1 & 1 & 6 & 18
\end{array}
\right]
\]

---

# Eliminasi Gauss (Segitiga Atas)

### Langkah 1
\[
R_1 \leftrightarrow R_2
\]

\[
\left[
\begin{array}{ccccc|c}
1 & 3 & 1 & 1 & 1 & 12 \\
2 & 1 & 1 & 1 & 1 & 10 \\
1 & 1 & 4 & 1 & 1 & 14 \\
1 & 1 & 1 & 5 & 1 & 16 \\
1 & 1 & 1 & 1 & 6 & 18
\end{array}
\right]
\]

---

### Langkah 2
\[
R_2 - 2R_1,\; R_3 - R_1,\; R_4 - R_1,\; R_5 - R_1
\]

\[
\left[
\begin{array}{ccccc|c}
1 & 3 & 1 & 1 & 1 & 12 \\
0 & -5 & -1 & -1 & -1 & -14 \\
0 & -2 & 3 & 0 & 0 & 2 \\
0 & -2 & 0 & 4 & 0 & 4 \\
0 & -2 & 0 & 0 & 5 & 6
\end{array}
\right]
\]

---

### Langkah 3
\[
R_2 = -\frac{1}{5}R_2
\]

\[
\left[
\begin{array}{ccccc|c}
1 & 3 & 1 & 1 & 1 & 12 \\
0 & 1 & \frac{1}{5} & \frac{1}{5} & \frac{1}{5} & \frac{14}{5} \\
0 & -2 & 3 & 0 & 0 & 2 \\
0 & -2 & 0 & 4 & 0 & 4 \\
0 & -2 & 0 & 0 & 5 & 6
\end{array}
\right]
\]

---

### Langkah 4
\[
R_3 + 2R_2,\; R_4 + 2R_2,\; R_5 + 2R_2
\]

\[
\left[
\begin{array}{ccccc|c}
1 & 3 & 1 & 1 & 1 & 12 \\
0 & 1 & \frac{1}{5} & \frac{1}{5} & \frac{1}{5} & \frac{14}{5} \\
0 & 0 & \frac{17}{5} & \frac{2}{5} & \frac{2}{5} & \frac{38}{5} \\
0 & 0 & \frac{2}{5} & \frac{22}{5} & \frac{2}{5} & \frac{48}{5} \\
0 & 0 & \frac{2}{5} & \frac{2}{5} & \frac{27}{5} & \frac{58}{5}
\end{array}
\right]
\]

---

### Langkah 5
\[
R_3 = \frac{5}{17}R_3
\]

\[
\left[
\begin{array}{ccccc|c}
1 & 3 & 1 & 1 & 1 & 12 \\
0 & 1 & \frac{1}{5} & \frac{1}{5} & \frac{1}{5} & \frac{14}{5} \\
0 & 0 & 1 & \frac{2}{17} & \frac{2}{17} & \frac{38}{17} \\
0 & 0 & \frac{2}{5} & \frac{22}{5} & \frac{2}{5} & \frac{48}{5} \\
0 & 0 & \frac{2}{5} & \frac{2}{5} & \frac{27}{5} & \frac{58}{5}
\end{array}
\right]
\]

---

### Langkah 6
\[
R_4 - \frac{2}{5}R_3,\; R_5 - \frac{2}{5}R_3
\]

\[
\left[
\begin{array}{ccccc|c}
1 & 3 & 1 & 1 & 1 & 12 \\
0 & 1 & \frac{1}{5} & \frac{1}{5} & \frac{1}{5} & \frac{14}{5} \\
0 & 0 & 1 & \frac{2}{17} & \frac{2}{17} & \frac{38}{17} \\
0 & 0 & 0 & 4 & 0 & 4 \\
0 & 0 & 0 & 0 & 5 & 5
\end{array}
\right]
\]

---

## Hasil Segitiga Atas

\[
\left[
\begin{array}{ccccc|c}
1 & 3 & 1 & 1 & 1 & 12 \\
0 & 1 & \frac{1}{5} & \frac{1}{5} & \frac{1}{5} & \frac{14}{5} \\
0 & 0 & 1 & \frac{2}{17} & \frac{2}{17} & \frac{38}{17} \\
0 & 0 & 0 & 4 & 0 & 4 \\
0 & 0 & 0 & 0 & 5 & 5
\end{array}
\right]
\]

---

# Eliminasi Gauss–Jordan

### Langkah 1
\[
R_5 = \frac{1}{5}R_5
\]

### Langkah 2
\[
R_1 - R_5,\; R_2 - \frac{1}{5}R_5,\; R_3 - \frac{2}{17}R_5
\]

### Langkah 3
\[
R_4 = \frac{1}{4}R_4
\]

### Langkah 4
\[
R_1 - R_4,\; R_2 - \frac{1}{5}R_4,\; R_3 - \frac{2}{17}R_4
\]

### Langkah 5
\[
R_1 - R_3,\; R_2 - \frac{1}{5}R_3
\]

### Langkah 6
\[
R_1 - 3R_2
\]

---

## Hasil Akhir (RREF)

\[
\left[
\begin{array}{ccccc|c}
1 & 0 & 0 & 0 & 0 & 2 \\
0 & 1 & 0 & 0 & 0 & 2 \\
0 & 0 & 1 & 0 & 0 & 2 \\
0 & 0 & 0 & 1 & 0 & 1 \\
0 & 0 & 0 & 0 & 1 & 1
\end{array}
\right]
\]

---

## Solusi

\[
\begin{aligned}
x &= 2 \\
y &= 2 \\
z &= 2 \\
w &= 1 \\
v &= 1
\end{aligned}
\]