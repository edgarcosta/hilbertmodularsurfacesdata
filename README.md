# hilbertmodularsurfacesdata

```
$ for i in joblog/*  ; do echo $i; awk -v OFMT=%.5g -F' ' '{sum+=$4;} END{print sum;}' $i; done
joblog/GL_Gamma0_lt3000_cut5000_cusps.txt
2261.7
joblog/GL_Gamma0_lt3000_cut5000_inv.txt
5001.4
joblog/SL_Gamma0_lt3000_cut5000_cusps.txt
2285
joblog/SL_Gamma0_lt3000_cut5000_inv.txt
4121.8
```
