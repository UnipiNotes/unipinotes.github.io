---
layout: class
title: Αρχές και Εφαρμογές Σημάτων και Συστημάτων | Theory Notes
slug: signals-theory
categories: second-year fourth-semester
sf: second-year/fourth-semester
katex: True
---

# Αρχές και Εφαρμογές Σημάτων και Συστημάτων [Matlab]
## Theory Notes

<br />

## Σήματα συνεχούς χρόνου

Η πρώτη κατηγορία  είναι τα `ημιτονοειδή σήματα`. Τα σήματα αυτά έχουν μία απλή μορφή:

$$x(t) = A cos(\Omega t + \theta)$$

**$$\Omega$$**: είναι η γωνιακή συχνότητα.

**$$A$$**: είναι το εύρος του σήματος μας.

**$$\theta$$**: είναι η ακτίνα σε rads.

Τα ημιτονοειδή σήματα είναι περιοδικά σήματα και η περίοδος $$ T $$ υπολογίζεται:

$$T = 2\pi / \Omega$$

Παράδειγμα:

Να σχεδιάσουμε το σήμα:

$$
x(t) = cos(100\pi t) + cos(200\pi t) + sin(500\pi t)
$$

όταν $$t \in [-10, 10]$$ και βήμα $$\Delta t = 0,001$$.


```matlab
omega1 = 100*pi;
omega2 = 200*pi;
omega3 = 500*pi;
t = -0.1:0.001:0.1;
x = cos(omega1*t) + cos(omega2*t) + sin(omega3*t);
plot(t,x);
xlabel("time");
ylabel("x(t)");
```

Στην περίπτωση μας δεν χρειάζεται να υπολογίσουμε το $$A$$ και το $$\theta$$ καθώς $$A= 1 \ \theta = 0$$.
