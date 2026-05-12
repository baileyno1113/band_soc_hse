# band_soc_hse
第一步PBE自洽：
HSE06杂化泛函计算能带需求权重为0的k点，先处理KPOINTS文件，以2D hexagon为例，首先依次输入vaspkit→302选择高对称点路径，注意与下面论文匹配
然后依次输入vaspkit→251→2→0.03→0.03
vaspkit INCAR H6
hse+soc:首先需要做一步带SOC的自洽计算:
#### SOC ####
LSORBIT = .TRUE.
SAXIS = 0 0 1
MAGMOM = 1000*0
GGA_COMPAT = .FALSE.
#---for slabs---#
#AMIX = 0.2
#BMIX = 0.00001
#LSCALAPACK = .FALSE. 
