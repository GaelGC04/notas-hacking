## Descripción
We made a lot of substitutions to encrypt this. Can you decrypt it? Connect with `nc jupiter.challenges.picoctf.org 39894`.

## Solución
Se hace nc a la máquina y se obtiene lo siguiente:
```
updikflr nbkb cr epxk hzfi - hkbwxbdue_cr_u_pqbk_zfjsgf_fihzuilexb
-------------------------------------------------------------------------------
sblobbd xr lnbkb ofr, fr c nfqb fzkbfge rfcg rpjbonbkb, lnb spdg ph lnb rbf. sbrcgbr npzgcdi pxk nbfklr lpiblnbk lnkpxin zpdi mbkcpgr ph rbmfkflcpd, cl nfg lnb bhhbul ph jfvcdi xr lpzbkfdl ph bfun plnbk'r efkdrfdg bqbd updqculcpdr. lnb zfoebklnb sbrl ph pzg hbzzpornfg, sbufxrb ph ncr jfde ebfkr fdg jfde qcklxbr, lnb pdze uxrncpd pd gbuv, fdg ofr zecdi pd lnb pdze kxi. lnb fuupxdlfdl nfg skpxinl pxl fzkbfge f spa ph gpjcdpbr, fdg ofr lpecdi fkunclbulxkfzze ocln lnb spdbr. jfkzpo rfl ukprr-zbiibg kcinl fhl, zbfdcdi fifcdrl lnb jcyybd-jfrl. nb nfg rxdvbd unbbvr, f ebzzpo upjmzbacpd, f rlkfcinl sfuv, fd frublcu frmbul, fdg, ocln ncr fkjr gkpmmbg, lnb mfzjr ph nfdgr pxlofkgr, kbrbjszbg fd cgpz. lnb gckbulpk, rflcrhcbg lnb fdunpk nfg ippg npzg, jfgb ncr ofe fhl fdg rfl gpod fjpdirl xr. ob baunfdibg f hbo opkgr zfycze. fhlbkofkgr lnbkb ofr rczbdub pd spfkg lnb efunl. hpk rpjb kbfrpd pk plnbk ob gcg dpl sbicd lnfl ifjb ph gpjcdpbr. ob hbzl jbgclflcqb, fdg hcl hpk dplncdi sxl mzfucg rlfkcdi. lnb gfe ofr bdgcdi cd f rbkbdcle ph rlczz fdg bawxcrclb skczzcfdub. lnb oflbk rnpdb mfuchcufzze; lnb rve, oclnpxl f rmbuv, ofr f sbdcid cjjbdrcle ph xdrlfcdbg zcinl; lnb qbke jcrl pd lnb brrba jfkrn ofr zcvb f ifxye fdg kfgcfdl hfskcu, nxdi hkpj lnb oppgbg kcrbr cdzfdg, fdg gkfmcdi lnb zpo rnpkbr cd gcfmnfdpxr hpzgr. pdze lnb izppj lp lnb obrl, skppgcdi pqbk lnb xmmbk kbfunbr, sbufjb jpkb rpjskb bqbke jcdxlb, fr ch fdibkbg se lnb fmmkpfun ph lnb rxd.
```
Se usa un identificador de cifrado para saber que cifrado es Substitution Cipher
Se descifra y se obtiene el siguiente texto con la flag
```
-------------------------------------------------------------------------------
congrats here is your flag - frequency_is_c_over_lambda_agflcgtyue
-------------------------------------------------------------------------------
between us there was, as i have already said somewhere, the bond of the sea. besides holding our hearts together through long periods of separation, it had the effect of making us tolerant of each other's yarnsand even convictions. the lawyerthe best of old fellowshad, because of his many years and many virtues, the only cushion on deck, and was lying on the only rug. the accountant had brought out already a box of dominoes, and was toying architecturally with the bones. marlow sat cross-legged right aft, leaning against the mizzen-mast. he had sunken cheeks, a yellow complexion, a straight back, an ascetic aspect, and, with his arms dropped, the palms of hands outwards, resembled an idol. the director, satisfied the anchor had good hold, made his way aft and sat down amongst us. we exchanged a few words lazily. afterwards there was silence on board the yacht. for some reason or other we did not begin that game of dominoes. we felt meditative, and fit for nothing but placid staring. the day was ending in a serenity of still and exquisite brilliance. the water shone pacifically; the sky, without a speck, was a benign immensity of unstained light; the very mist on the essex marsh was like a gauzy and radiant fabric, hung from the wooded rises inland, and draping the low shores in diaphanous folds. only the gloom to the west, brooding over the upper reaches, became more sombre every minute, as if angered by the approach of the sun.

```
Se tiene que la flag tiene un formato distinto sin el `picoCTF{}`

```
frequency_is_c_over_lambda_agflcgtyue
```

## Referencias:
* https://www.boxentriq.com/code-breaking/cipher-identifier
* https://www.boxentriq.com/code-breaking/substitution-cipher