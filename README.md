# hilbertmodularsurfacesdata

```
$ for i in joblog/*  ; do echo $i; awk -v OFMT=%.17g -F' ' '{sum+=$4;} END{print sum;}' $i; done
joblog/GL_Gamma0_lt3000_cut5000_cusps.txt
3239.6029999999823
joblog/GL_Gamma0_lt3000_cut5000_hs.txt
540139.64800000004
joblog/GL_Gamma0_lt3000_cut5000_inv.txt
6267.4210000000239
joblog/GL_Gamma0_lt3000_cut5000_kposs.txt
6341.840999999994
joblog/SL_Gamma0_lt3000_cut5000_cusps.txt
3151.7949999999987
joblog/SL_Gamma0_lt3000_cut5000_inv.txt
5541.5460000000039
joblog/SL_Gamma0_lt3000_cut5000_kposs.txt
5561.1489999999931
```
