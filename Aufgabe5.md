## Aufgabe 5: Gegeben sei die Differentialgleichung zweiter Ordnung

$$
\ddot{x}(t) = \frac{1}{3}x^2(t) - 3\cos(\dot{x}(t)) - 5\dot{x}(t)
$$

### Part (a)
Schreiben Sie (1) um in ein System von Differentialgleichungen erster Ordnung.

Zur Umwandlung dieser Gleichung in ein System erster Ordnung führen wir eine neue Variable ein:
$$
y_1 = x(t), \quad y_2 = \dot{x}(t)
$$

Dann kann die ursprüngliche Gleichung zweiter Ordnung geschrieben werden als:
$$
\dot{y}_1 = y_2
$$
$$
\dot{y}_2 = \frac{1}{3}y_1^2 - 3\cos(y_2) - 5y_2
$$

Somit ist das System erster Ordnung:
$$
\begin{cases}
\dot{y}_1 = y_2 \\
\dot{y}_2 = \frac{1}{3}y_1^2 - 3\cos(y_2) - 5y_2
\end{cases}
$$

Wir können dies als:
$$
\vec{\dot{y}} = \begin{pmatrix}
\dot{y}_1 \\
\dot{y}_2
\end{pmatrix} = \begin{pmatrix}
y_2 \\
\frac{1}{3}y_1^2 - 3\cos(y_2) - 5y_2
\end{pmatrix} = \vec{F}(\vec{y})
$$

### Part (b)
Bestimmen Sie alle Gleichgewichtspunkte des Systems.

Gleichgewichtspunkte \(\vec{y}_e\) werden gefunden, indem man \(\vec{\dot{y}} = 0\) setzt:
$$
\begin{cases}
\dot{y}_1 = y_2 = 0 \\
\dot{y}_2 = \frac{1}{3}y_1^2 - 3\cos(y_2) - 5y_2 = 0
\end{cases}
$$

Durch Einsetzen von \(y_2 = 0\) in die zweite Gleichung:
$$
\frac{1}{3}y_1^2 - 3\cos(0) - 5(0) = 0 \implies \frac{1}{3}y_1^2 - 3 = 0 \implies y_1^2 = 9 \implies y_1 = \pm 3
$$

Also sind die Gleichgewichtspunkte:
$$
\vec{y}_e = \begin{pmatrix}
3 \\
0
\end{pmatrix} \quad \text{und} \quad \vec{y}_e = \begin{pmatrix}
-3 \\
0
\end{pmatrix}
$$

### Part (c)
Bestimmen Sie die Art und Stabilität der Gleichgewichtspunkte durch Analyse der Eigenwerte des linearisierten Systems.

Um das System um einen Gleichgewichtspunkt \(\vec{y}_e\) zu linearisieren, berechnen wir die Jacobi-Matrix \(J\) von \(\vec{F}(\vec{y})\):
$$
J = \begin{pmatrix}
\frac{\partial F_1}{\partial y_1} & \frac{\partial F_1}{\partial y_2} \\
\frac{\partial F_2}{\partial y_1} & \frac{\partial F_2}{\partial y_2}
\end{pmatrix} = \begin{pmatrix}
0 & 1 \\
\frac{2}{3}y_1 & 3\sin(y_2) - 5
\end{pmatrix}
$$

Die Jacobi-Matrix wird an jedem Gleichgewichtspunkt ausgewertet.

Für \(\vec{y}_e = \begin{pmatrix}
3 \\
0
\end{pmatrix}\):
$$
J = \begin{pmatrix}
0 & 1 \\
2 & -5
\end{pmatrix}
$$

Für \(\vec{y}_e = \begin{pmatrix}
-3 \\
0
\end{pmatrix}\):
$$
J = \begin{pmatrix}
0 & 1 \\
-2 & -5
\end{pmatrix}
$$

Die Eigenwerte einer Matrix \(A\) werden durch Lösung von \(\det(A - \lambda I) = 0\) gefunden.

#### Eigenwerte für \(\vec{y}_e = \begin{pmatrix} 3 \\ 0 \end{pmatrix}\):
Lösen Sie für \(\lambda\) in:
$$
\det\begin{pmatrix}
-\lambda & 1 \\
2 & -5 - \lambda
\end{pmatrix} = 0 \implies \lambda^2 + 5\lambda - 2 = 0
$$

Die Lösungen sind:
$$
\lambda = \frac{-5 \pm \sqrt{25 + 8}}{2} = \frac{-5 \pm \sqrt{33}}{2}
$$

Da die Eigenwerte beide einen negativen Realteil haben, ist das Gleichgewicht bei \(\begin{pmatrix} 3 \\ 0 \end{pmatrix}\) ein stabiler Fokus.

#### Eigenwerte für \(\vec{y}_e = \begin{pmatrix} -3 \\ 0 \end{pmatrix}\):
Lösen Sie für \(\lambda\) in:
$$
\det\begin{pmatrix}
-\lambda & 1 \\
-2 & -5 - \lambda
\end{pmatrix} = 0 \implies \lambda^2 + 5\lambda + 2 = 0
$$

Die Lösungen sind:
$$
\lambda = \frac{-5 \pm \sqrt{25 - 8}}{2} = \frac{-5 \pm \sqrt{17}}{2}
$$

Da die Eigenwerte beide einen negativen Realteil haben, ist das Gleichgewicht bei \(\begin{pmatrix} -3 \\ 0 \end{pmatrix}\) ein stabiler Fokus.

Zusammenfassend:
- Die Gleichgewichtspunkte des Systems sind \(\begin{pmatrix} 3 \\ 0 \end{pmatrix}\) und \(\begin{pmatrix} -3 \\ 0 \end{pmatrix}\).
- Beide Gleichgewichtspunkte sind stabile Fokusse.
