# Варианты заданий к лабораторным работам
## Метод цепочек

Вариант 1:
```pascal
ACCEPT *; A
if  (A.LE.0)  S=S+A
S=A*100-K
```

Вариант 2:
```pascal
МАХ=0
if (X.GT.MAX) MAX=X 
TYPE *,  MAX
```

Вариант 3:
```pascal
D=B*B=-4*A*C 
if (D.EQ.O) T=-B/(2*A)
TYPE*, T
```

Вариант 4:
```pascal
S1:=A MOD B;
S2:=A-((A DIV B)*B);
if   S1=S2 then write ('ВСЁ')
```

Вариант 5:
```pascal
if x>0 then y:=l
else if x<0 then y:=2
else y:=0
```

Вариант 6:
```pascal
if Y>MIN & Y<MAX then 
PUT LIST (Y);
else X=X+1;
```

Вариант 7:
```pascal
Z=Z+1;
if Z>N then DO;
Z=Z/N; 
PUT DATA (Z); 
end;
```

Вариант 8:
```pascal
X=X0+(i-l)*H 
if (X.LT.O)  Y=X*X
if  (X.GT.O)  Y=2*X
```
Вариант 9:
```pascal
if i MOD 2=0 THEN Z:=Z*X;
i:=i DIY 2; 
X:=X*X*X
```

Вариант 10:
```pascal
READ(B); 
if B>L THEN begin
A:=A-Z;
A:=A+B end
else B:=L+B
```

Вариант 11:
```pascal
if (X+Y)<>0 THEN
A:=(X*X+Z*Z)/(1 +1/(X-Y*Z))
else A:=0;
writeln (A)
```

Вариант 12:
```pascal
A:=-3*C;
B:=Y*Y*X;
if (A<0) AND (B>0) THEN
C:=-A+B 
else C:=A+B

```

Вариант 13:
```pascal
if  T>EPS THEN begin 
K:=K+2; 
T:=-T*SX/(K*(K-1));
S:=S+T
end
```

Вариант 14:
```pascal
if N>0 THEN
M:=-M+l/N; 
B:=M*N+3; 
if B=0 THEN write (N)
```

Вариант 15:
```pascal
if  (2.5+0.68<=2.8) OR Y
AND X OR Z AND NOT Y THEN
writeln ('верно')
```

Вариант 16:
```pascal
READ(N);
M:=0;
If f=1 THEN writeln (M)
Else M:=M+1/N
```

Вариант 17:
```pascal
RESET (F,’F.DAT’);
SUM:=SUM+F^; 
GET (F)
```

Вариант 18:
```pascal
REWRITE (F, 'F.DAT'); 
F^:=K*K; 
PUT (F)
```

Вариант 19:
```pascal
READ (x, y);
A:=x/(y*y*x*x/(y+x/3))
```

Вариант 20:
```pascal
READ (H, В, М);
PI:=3.14; 
V:=PI*H*(B*B+M*M+B*M)/3
```

Вариант 21:
```pascal
A=Z*Z;
B=l+A/(3*Z+A/5);
if B>5 THEN writeln (B)
```

Вариант 22:
```pascal
if x<0.5 THEN y=2*x*x-x 
else y=x*x/(x-0.1); 
write (y)
```

Вариант 23:
```pascal
READ (A, B);
IF A>B THEN X=2*A+2/B+4; 
IF A<=B THEN x=(A+B)*(A-B);
writeln (x)
```

Вариант 24:
```pascal
READ (I);
if (I>4) OR (I<0) THEN
writeln ('ошибка')
```

Вариант 25:
```pascal
if A<0 THEN A=-A;
if B<0 THEN B=-B;
SA:=(A+B)/2;
SB:=A*B/2
```

Вариант 26:
```pascal
READLN (Y); 
if Y<0 THEN
Z:=Y-3*Y*Y/(Y+1)
else if Y=0 THEN Z:=0 
else Z:=100*Y
```
