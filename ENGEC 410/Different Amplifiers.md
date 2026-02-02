### Cascode Amplifier
A current source connected to two MOSFETs in parallel. 

![[Pasted image 20251112145758.png]]

```
v=i7ro
r1=r0
r2=(gm*r0)r0
r3=(r2+r0)/(gm*r0)
  =(gmr0^2+r0)/gmr0
  =r0+1/gm=r0

i1 = gmvi
i2 = i1 * (r3 / r3 + r0)
i3 = i1 / 2
i4 = i3 = i5 = i7 = i2
i6 = 0 (gs grounded)
v1 = -gmr0/2 * vi (50 mV peak)
v2 = -i2r2 = (gmr0)^2/2 * vi (1V peak)
v3 = -i5r1 = -gmr0/2 * vi (50 mV peak)
```

### Differential Amplifier

```
v_d1 = vdd - id1 * RD
v_d2 = vdd - id2 * RD
idx = gm * v_gs
vo = v_d1 - v_d2 = -(id1 - id2) * RD
  = -gm * RD * (v_g1 - vg2)
```

If a common mode was established:
```
vgs = vcm - vs = vt + vov
I/2 = Ids
vd1 = vd2 = vdd - RdI/2
vo = 0
```

If there was a small input signal difference:
```
id1 = gm * vgs
id2 = -gm * vs
vo = gm * rd * vg
```

```
id=I/2 +- (I/Vov)(vid/2)q(1-(vd/2)2/vov2)
```