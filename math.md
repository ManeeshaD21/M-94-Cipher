Suppose you intercept a message, and you know the sender is using a Caesar cipher, but do not know the shift being used. The message begins EQZP. How hard would it be to decrypt this message?

Solution

Since there are only 25 possible shifts, we would only have to try 25 different possibilities to see which one produces results that make sense. While that would be tedious, one person could easily do this by hand in a few minutes. A modern computer could try all possibilities in under a second.

 𝐒𝐡𝐢𝐟𝐭 123456 𝐌𝐞𝐬𝐬𝐚𝐠𝐞  DPYO  COXN  BNWM  AMVL  ZLUK  YKTJ  𝐒𝐡𝐢𝐟𝐭 789101112 𝐌𝐞𝐬𝐬𝐚𝐠𝐞  XJSI  WIRH  VHQG  UGPF  TFOE  𝐒𝐄𝐍𝐃  𝐒𝐡𝐢𝐟𝐭 131415161718 𝐌𝐞𝐬𝐬𝐚𝐠𝐞  RDMC  QCLB  PBKA  OAJZ  NZIY  MYHX  𝐒𝐡𝐢𝐟𝐭 19202122232425 𝐌𝐞𝐬𝐬𝐚𝐠𝐞  LXGW  KWFV  JVEU  IUDT  HTCS  GSBR  FRAQ  
 Shift 
 Message 
 Shift 
 Message 
 Shift 
 Message 
 Shift 
 Message 
1	 DPYO 	7	 XJSI 	13	 RDMC 	19	 LXGW 	2	 COXN 	8	 WIRH 	14	 QCLB 	20	 KWFV 	3	 BNWM 	9	 VHQG 	15	 PBKA 	21	 JVEU 	4	 AMVL 	10	 UGPF 	16	 OAJZ 	22	 IUDT 	5	 ZLUK 	11	 TFOE 	17	 NZIY 	23	 HTCS 	6	 YKTJ 	
1
2
 SEND 
18	 MYHX 	24	 GSBR 							25	 FRAQ   

In this case, a shift of 12 (A mapping to M) decrypts EQZP to SEND. Because of this ease of trying all possible encryption keys, the Caesar cipher is not a very secure encryption method.
