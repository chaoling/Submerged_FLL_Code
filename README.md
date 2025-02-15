# Derivation of the Turning Radius Formula for a Differential-Drive Robot

## 1. Understanding the Geometry

Consider a differential-drive robot with:
- **Axle Track (\(d\))**: The distance between the two wheels.
- **Robot’s Center**: The midpoint between the wheels.
- **Turning Center**: The point around which the robot rotates.

When the robot turns:
- The **left wheel** follows a circular path with radius:  
  \[
  R_{\text{left}} = R + \frac{d}{2}
  \]
- The **right wheel** follows a circular path with radius:  
  \[
  R_{\text{right}} = R - \frac{d}{2}
  \]
where \(R\) is the distance from the robot’s center to the turning center.

## 2. Relating Linear and Angular Velocities

For circular motion, the linear velocity \(v\) is related to the angular velocity \(\omega\) and the radius \(r\) by:
\[
v = \omega \, r
\]

Thus, the linear speeds for the two wheels are:
- **Left Wheel:**
  \[
  v_{\text{left}} = \omega \left(R + \frac{d}{2}\right)
  \]
- **Right Wheel:**
  \[
  v_{\text{right}} = \omega \left(R - \frac{d}{2}\right)
  \]

## 3. Expressing the Difference in Speeds

Subtract the equation for the right wheel from that of the left wheel:
\[
v_{\text{left}} - v_{\text{right}} = \omega \left[\left(R + \frac{d}{2}\right) - \left(R - \frac{d}{2}\right)\right]
\]
Simplify the expression:
\[
v_{\text{left}} - v_{\text{right}} = \omega \, d
\]
Solve for \(\omega\):
\[
\omega = \frac{v_{\text{left}} - v_{\text{right}}}{d}
\]

## 4. Expressing the Average Speed

Add the two equations for the left and right wheels:
\[
v_{\text{left}} + v_{\text{right}} = \omega \left[\left(R + \frac{d}{2}\right) + \left(R - \frac{d}{2}\right)\right]
\]
Simplify:
\[
v_{\text{left}} + v_{\text{right}} = \omega (2R)
\]
Solve for \(R\):
\[
R = \frac{v_{\text{left}} + v_{\text{right}}}{2\omega}
\]

## 5. Substituting \(\omega\) into the Expression for \(R\)

Substitute the expression for \(\omega\) from step 3 into the equation for \(R\):
\[
R = \frac{v_{\text{left}} + v_{\text{right}}}{2 \left(\frac{v_{\text{left}} - v_{\text{right}}}{d}\right)}
\]
Simplify by multiplying the numerator and denominator:
\[
R = \frac{v_{\text{left}} + v_{\text{right}}}{\frac{2(v_{\text{left}} - v_{\text{right}})}{d}} = \frac{d}{2} \times \frac{v_{\text{left}} + v_{\text{right}}}{v_{\text{left}} - v_{\text{right}}}
\]

## 6. Final Formula

The turning radius \(R\) is:
\[
\boxed{R = \frac{d}{2} \times \frac{v_{\text{left}} + v_{\text{right}}}{v_{\text{left}} - v_{\text{right}}}}
\]

---

## Important Notes:
- **Straight Movement:** When \(v_{\text{left}} = v_{\text{right}}\), the denominator is zero, indicating the robot moves in a straight line (i.e., \(R \to \infty\)).
- **Turning Direction:** The sign of \(v_{\text{left}} - v_{\text{right}}\) determines the direction of the turn.
- **Axle Track Impact:** A larger axle track \(d\) will increase the turning radius for a given set of motor speeds.