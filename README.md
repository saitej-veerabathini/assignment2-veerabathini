# assignment2-veerabathini
# Saitej Veerabathini
###### London

London, the capital of England and the United Kingdom, is a 21st-century city with history stretching back to **Roman times**. At its centre stand the imposing Houses of Parliament, the iconic ‘Big Ben’ clock tower and Westminster Abbey, site of British monarch coronations. **Across the Thames River, the London Eye observation wheel provides panoramic views of the South Bank cultural complex, and the entire city.**

---

# Directions To London

1. Take a cab to Kansas Airport.
    1. Check in your baggage.
    2. Clear Security Checking.
    3. Wait until your boarding time.
2. Layover at Chicago.
    1. Go to the respective terminal.
    2. If there is a need for TSA checking, get clear with it.
    3. Go to the respective Gate number.
    4. Board flight to London.
3. Arrival at London.
    1. Get your baggage at the baggage belt.
    2. Hire a cab to your accommodation.

# Items To Be Carried For Maximum Enjoyment.

* Camera.
* Clothes.
* Food items.
* Extra Batteries.

---

**[About Me](AboutMe.md)**

---

### Hungry?

Now that you're hungry here are some of the  mouth-watering food items that no one can resist to. This table gives information about the famous food items that are available in different parts of India.

| Item | Location | Amount |
| :---: | :---:    | :---:   |
| Biryani | Hyderabad | $3 |
| Paav Bhaji | Mumbai | $1 |
| Lassi | Punjab | $1 |
| Paratha | Delhi | $2 |

---
### Some Quotes..

>An eye for an eye makes the whole world blind.
*-Mahatma Gandhi*

>You cannot believe in God until you believe in yourself. 
*-Swami Vivekananda*

---
 
# Intersection of two points:

>When two lines share exactly one common point, they are called the intersecting lines. The intersecting lines share a common point. And, this common point that exists on all intersecting lines is called the point of intersection. The two non-parallel straight lines which are co-planar will have an intersection point. 
Link: <https://www.cuemath.com/geometry/intersection-of-two-lines/>

```java
struct pt {
    double x, y;
};

struct line {
    double a, b, c;
};

const double EPS = 1e-9;

double det(double a, double b, double c, double d) {
    return a*d - b*c;
}

bool intersect(line m, line n, pt & res) {
    double zn = det(m.a, m.b, n.a, n.b);
    if (abs(zn) < EPS)
        return false;
    res.x = -det(m.c, m.b, n.c, n.b) / zn;
    res.y = -det(m.a, m.c, n.a, n.c) / zn;
    return true;
}

bool parallel(line m, line n) {
    return abs(det(m.a, m.b, n.a, n.b)) < EPS;
}

bool equivalent(line m, line n) {
    return abs(det(m.a, m.b, n.a, n.b)) < EPS
        && abs(det(m.a, m.c, n.a, n.c)) < EPS
        && abs(det(m.b, m.c, n.b, n.c)) < EPS;
}
```
Link: <https://cp-algorithms.com/geometry/lines-intersection.html>




