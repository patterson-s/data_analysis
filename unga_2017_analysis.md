``` r
pacman::p_load(stm,
               dplyr,
               quanteda,
               readr)

# set.seed
set.seed(420)
```

Load Data for githubdoc
=======================

``` r
load("myEnvironment.RData")
```

Content
=======

``` r
t0_k12_cont_EU_topics <- labelTopics(t0_k12_cont_EU, n = 20)

plot(t0_k12_cont_EU, type = "perspectives", topics = 1)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k12_cont_EU-1.png)

``` r
plot(t0_k12_cont_EU, type = "perspectives", topics = 2)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k12_cont_EU-2.png)

``` r
plot(t0_k12_cont_EU, type = "perspectives", topics = 3)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k12_cont_EU-3.png)

``` r
plot(t0_k12_cont_EU, type = "perspectives", topics = 4)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k12_cont_EU-4.png)

``` r
plot(t0_k12_cont_EU, type = "perspectives", topics = 5)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k12_cont_EU-5.png)

``` r
plot(t0_k12_cont_EU, type = "perspectives", topics = 6)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k12_cont_EU-6.png)

``` r
plot(t0_k12_cont_EU, type = "perspectives", topics = 7)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k12_cont_EU-7.png)

``` r
plot(t0_k12_cont_EU, type = "perspectives", topics = 8)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k12_cont_EU-8.png)

``` r
plot(t0_k12_cont_EU, type = "perspectives", topics = 9)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k12_cont_EU-9.png)

``` r
plot(t0_k12_cont_EU, type = "perspectives", topics = 10)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k12_cont_EU-10.png)

``` r
plot(t0_k12_cont_EU, type = "perspectives", topics = 11)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k12_cont_EU-11.png)

``` r
plot(t0_k12_cont_EU, type = "perspectives", topics = 12)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k12_cont_EU-12.png)

``` r
labelTopics(t0_k18_cont_EU, n = 20)
```

    ## Topic Words:
    ##  Topic 1: kohl, honeck, erich, space-bas, abm, german-polish, helmut, german, responsi¬bl, pan-european, situa¬t, andropov, persh, cmea, states-soviet, con¬tinu, intermediate-rang, honak, ural, good-neighbor 
    ##  Topic 2: l’aquila, johnson-sirleaf, himalayan, rights-bas, cybercrim, climate-resili, att, michell, bachelet, gordon, peacebuild, cyber, -track, childbirth, community-bas, obama’, pittsburgh, busan, arctic, tsunami 
    ##  Topic 3: tit, rumor, egyptian-isra, indo-china—, tween, late—, roger, heng, samrin, vaniti, tion, regime-, brillianc, gromyko, ultima, indochina, seychell, kissing, lndo-china, re-divid 
    ##  Topic 4: tempest, fathom, ungovern, indec, foul, plug, kennedi, thick, shred, glass, tyrant, thunder, roll-cal, sync, scari, metropoli, self-lov, unmoor, yanukovych, spinoza 
    ##  Topic 5: todayâ, rapid-react, cost-cut, “cultur, aconf, unpaid, slavonia, standbi, kinkel, fiftieth-anniversari, high-readi, tribunal’, dual-us, ecosoc, “supplement, anti-personnel, peace-enforc, stand-, secretariat’, robinson 
    ##  Topic 6: staffan, ross, syrian, lakhdar, refugees’, abdulaziz, syria’, daesh, león, syria, nassir, kerri, vuk, respres, al-nass, two-stat, bahraini, abadi, work”, al-abadi 
    ##  Topic 7: marcoussi, kivu, bunia, libérat, fnl, monuc, national, somalian, codesa, inter-congoles, unami, congoles, mouvement, africa-europ, booby-trap, circumcis, eufor, monuc’, artemi, kinshasa 
    ##  Topic 8: peace¬keep, recog¬n, habib, con¬cern, lebanon—, par¬ticular, responsi¬bl, situa¬t, obduraci, israel—, terri¬tori, coun¬tri, interna¬t, governments—, hag, con¬sider, accord¬, con¬tinu, con¬vent, flimsi 
    ##  Topic 9: nkomati, sadcc, imp, contadora, shorter-rang, population—, pan-africanist, gbadolit, south-north, pre-implement, pinié, bophuthatswana, venda, catalog, intermediate-rang, bast, internationalis, ifad, problems—, non-whit 
    ##  Topic 10: chapultepec, minurso, minugua, guatemalteca, unidad, mitch, sfor, hunan, andorra, revolucionaria, reincorpor, urng, “agenda, stabilis, bahía, radicalis, croatian-muslim, long-tem, mallorca, ghali 
    ##  Topic 11: varosha, bizon, ankara, papandreou, famagusta, cypriot, greek, bi-zon, turkish-cypriot, turkey’, turkish, lausann, bi-commun, bicommun, aegean, situation—, turkey, aguirr, greek-turkish, greec 
    ##  Topic 12: nonnuclear, mekong, countries—develop, hartl, scone, -white, hope-giv, slang, number-, commit-, seyn, cut-back, longterm, assis¬t, developed—, war-tim, revitalis, mcnamara, multiyear, aiaddl 
    ##  Topic 13: isil, al-assad’, bashar, dilma, bisexu, transgend, rousseff, history’, gay, synagogu, al-assad, islamist, else’, daesh, clone, stiglitz, third-largest, wake-, beslan, rouhani’ 
    ##  Topic 14: virgilio, argentinean, varga, barco, bradi, amort, wide¬spread, bruntland, felip, lender, tela, refinanc, lopez, portillo, plata, drape, argentina’, solitud, gonzalez, vitoria 
    ##  Topic 15: roger, smack, valeri, gairi, giscard, yaound, latin-american, gaull, spice, guide-lin, desta, us-, underwat, ahidjo, unplan, meetingj, gowon, well-understood, simplic, years- 
    ##  Topic 16: post-independ, chiluba, quota-fre, re-engag, life-sav, scotland, unmil, zimbabwean, baidoa, small-hold, sub-standard, land-min, garang, mahiga, childbirth, darfur, kenyan, ngara, “total, duty-fre 
    ##  Topic 17: romania’, bulgaria’, undcp, romanian, pristina, romania, transdniestria, nations-l, bulgaria, transregion, bratislava, ossetia, ctc, khatami, roma, fukushima, macedonia’, kosovar, karzai, opium 
    ##  Topic 18: chlorofluorocarbon, re-unif, rocard, micronesia, ocean-b, tlatelolco, capitalis, pew, liberalis, reforest, antarctica, ozon, westminst, marshal, minimis, law-mak, tropic, antarct, vessel, chemical-weapon 
    ##  
    ##  Covariate Words:
    ##  Group 0: restructur, legisl, expedit, complet, provis, includ, valuabl, isol, constitut, consult, various, sincer, implement, annal, gracious, date, believ, agreement, taken, initi 
    ##  Group 1: brdo, penalty”, teammat, responsibilities—, ever-recur, eroglu, liais, non-libyan, re-ignit, union-brok, “platform”, anastasiad, lubber, ruud, akıncı, reprofil, dimitri, fourier, intensity”, sophocl 
    ##  
    ##  Topic-Covariate Interactions:
    ##  Topic 1, Group 0: gierek, rapacki, presidium, husak, soviet-indian, soviet-french, songun, anti-reunif, pre-revolutionari, korea-unit, batmunkh, ilyich, politbureau, ceaugescu, tsedenb, freeze”, khural, anti-hitlerit, kosciuszko, parti¬cular 
    ##  Topic 1, Group 1: german-soviet, locomot, ecologically-ori, equalis, good-exampl, hop·, peace-inspir, stability-ori, cooperation—polit, hered, moscow—, punishment—, states—soon, verdun, vmf, aachen, aerosol, economy-ecolog, ícscr, molohi 
    ##  
    ##  Topic 2, Group 0: ldcs, non-communic, tuvalu’, lucia’, redd, reparatori, erika, grenada’, barbuda’, tonga’, oec, bangla, pan-caribbean, dominica’, barbudan, jamaica’, tobago’, jeann, ncds, ldc 
    ##  Topic 2, Group 1: cyberattack, aristotl, vilnius, estonian, estonia, estonia’, latvia, iceland’, lithuania, hammarskjöld, country-own, still-great, donorship, -earth, reverse”, transsexu, near-glob, chaghcharan, man-creat, sea-dump 
    ##  
    ##  Topic 3, Group 0: demarch, kampuchea-thailand, phen, pursat, battambang, awac, second-world, cham, sr-, kaishek, corinto, valparaiso, takeo, walker, hoang, glorieus, sinovietnames, sek, hua, kuo-feng 
    ##  Topic 3, Group 1: gierek, non-inflationari, also-inde, begun-, bremen, germany-berlin, germany-yesterday, liver, midst—solomon, participants-, sessions-, world—quit, cooperation—awar, process—without, secure—, years—doubl, andi, peace-cr, peace-preserv, alonb 
    ##  
    ##  Topic 4, Group 0: disempow, monoth, andorran, andorra’, pyrene, shakespear, saviour, vulgar, camera, smack, painless, vendetta, feather, jewel, belfast, vault, theolog, heresi, cathedr, aristotl 
    ##  Topic 4, Group 1: britain’, cfe, drone, tadeusz, zepa, dermatolog, fifth-centuri, flavius, flood’, hodel, lapland, pradesh, publius, reagan’, renatus’, sunglass, uttar, vegetius, wide-brim, will￼unfortun 
    ##  
    ##  Topic 5, Group 0: iceland’, monaco’, people-smuggl, slovakia, malta’, monaco, dividend”, war-affect, princess, chile’, “renew, reform”, “white, convention’, marino, protect”, unscom, canada’, slovak, nato’ 
    ##  Topic 5, Group 1: greenland, zepa, unamir, kabila’, herzegovina’, non-albanian, tyrol, bosnian, croat, tyrolean, salman, tashkent, untac, unprofor, hutu, forty-eighth, better-defin, ingvar, â€œto, denmarkâ 
    ##  
    ##  Topic 6, Group 0: egypt’, salman, melilla, al-nahyan, emirati, emirates’, al-saud, al-shareef, sa’dah, hadi, derna, tumb, shab’, yemen’, shaikh, mousa, al-shura, oman’, abidin, qaboo 
    ##  Topic 6, Group 1: malta’, boubacar, isi, guinea-bissau’, minsk, valletta, donba, séléka, non-communic, mali, malta, mali’, commission-leagu, marco’, israel-bash, human-rights-protect, political-diplomat, “nurs, diptych, jibreel 
    ##  
    ##  Topic 7, Group 0: séléka, mali’, kabila’, minurca, guinea-bissau’, malian, tutsi, houphouet-boigni, hutu, bangui, ondimba, togo’, senatori, mohéli, ange-félix, patassé, démocrati, inter-burundian, toumani, copax 
    ##  Topic 7, Group 1: unta, eleg, -pronounc, often-understand, shake-, braudel, capitalism, cold-heart, économi, fernand, matériell, lièg, outgam, calculation”, crate, haesendonck, razili, weu’, niass, casino-lik 
    ##  
    ##  Topic 8, Group 0: deir, tiran, jewri, qibya, shatt-al-arab, haaretz, mosh, kafr, khanaqin, barzani, basrah, weizmann, dayan, bani-sadr, shatt-el-arab, defac, judea, qasr-eshirin, fahmi, judaea 
    ##  Topic 8, Group 1: demarch, thai-kampuchean, argentin, africa-, area-includ, country-namibia-, emphasize-, involved-accept, limitations-, limited-posit, odious-, order-even, us-everi, bevin, english-languag, pro-duc, -promis, borrow—, just—world, long-canvass 
    ##  
    ##  Topic 9, Group 0: transkei, -payment, koevoet, traor, administrator-gener, turnhall, siaka, pac, ershad, apper, kountch, supremacist, jayewarden, chad-libya, seyni, carletonvill, afrikan, reed, kolingba, al-hadj 
    ##  Topic 9, Group 1: roh, egyptian-isra, acp-partn, case-fir, community-hungari, ecus, geroayel, h-saharan, institution·, one-point, re-acceler, apvpp-, cpc, frontiers·, hein, piet, plaid, single·, your, conflictand 
    ##  
    ##  Topic 10, Group 0: croatia, non-albanian, herzegovina’, croatia’, latvia, icti, marginalis, guido, croat, serbian, civilis, zagreb, herzegovina, liberalis, unta, lithuania, estonia, croatian, kosova, bosnia 
    ##  Topic 10, Group 1: spain’, gibraltar, spaniard, cplp, melilla, macao, spain, alioun, spanish, portuguese-speak, unita’, cruz, houphouet-boigni, santa, portugues, unita, arbitration-security-disarma, barcelona”, colony’, voter-identif 
    ##  
    ##  Topic 11, Group 0: tyrolean, tyrol, valletta, partitionist, enosi, greek-cypriot, spaniard, ataturk, kemal, state—, rill, ever-escal, austrian, kreiski, euro-mediterranean, austria, lazar, us-, mojsov, short-com 
    ##  Topic 11, Group 1: greece’, casus, islet, pan-american, island’, gambari, fahd, cypriot-own, talat’, “fact”, ciller, gávdhos, greek-bulgarian, ioannina, nesto, varna, cypriot-l, ankara’, clerides’, karpass 
    ##  
    ##  Topic 12, Group 0: roh, ecaf, nepal, arf, yen, bikram, bir, cambodia’, nam’, birendra, yasushi, dev, farakka, tae, wangchuck, nepales, singy, woo, jigm, pattaya 
    ##  Topic 12, Group 1: painless, jewri, antill, self-examin, transkei, allana, export-credit, outbalanc, recover, self-profess, sub-commission—must, assume-, banjak, convention-albeit, government-lik, jia, key-word, nations-tens, objective-, others-observ 
    ##  
    ##  Topic 13, Group 0: drone, chávez, isi, pakistan’, tamil, mohtarma, taliban’, evo, decertifi, ltte, lavala, herat, eelam, lanka’, hizbullah, benazir, kandahar, morazán, libel, raúl 
    ##  Topic 13, Group 1: blanco, feather, greek-cypriot, eisenhow, deir, nafusa, zawiyah, al-sheitaat, campuses”, enemies’, ez-zor, isil”, klansmen, quasi-mediaev, againlf, countrywomen, daraa, happen”, islamist-l, kleptocraci 
    ##  
    ##  Topic 14, Group 0: paz, argentin, brazil’, quito, peruvian, bánzer, lozada, zuazo, quechua, quetzal, belaund, coca-leaf, ecuador’, borja, zamora, peru’, bolivian, garcía, sánchez, portofspain 
    ##  Topic 14, Group 1: marginalis, cowri, migliuolo, needier, us-ussr, hispano-british, newly-recov, archenemi, bartoszewski, import-ori, self-giv, wladyslaw, itr, “hungari, communist-socialist, dumping”, nex, non-pot, “lead, canut 
    ##  
    ##  Topic 15, Group 0: edvard, anti-portugues, jean-bedel, trawler, vietcong, sakiet, dahomey, peron, brooksrandolph, uthant, viet-cong, lamizana, bokassa, unctadj, amphictyon, volta, german-soviet, president--lif, leopoldo, -equip 
    ##  Topic 15, Group 1: tiran, rapacki, caledonian, french-speak, hissein, yen, habr, beew, pie-judg, states-keep, stillwithin, successful-, kite, patience-admir, roza, settled-far, sir-presid, baudouin, debate-among, drama- 
    ##  
    ##  Topic 16, Group 0: amisom, unita’, al-bashir, abyei, renamo, ecomog, eritrean, sadc, unmiss, mkapa, liberia’, machako, badm, somaliaí, ruf, tanzania’, swaziland’, bowen, parpa, ethiopia’ 
    ##  Topic 16, Group 1: belfast, ira, unionist, anglo-irish, ireland, ireland’, obscen, irish, afrikan, decommiss, lankan, bankintern, compliance”, godana, post-lomé, burma’, aiken, lessons-learn, aiken’, rice’ 
    ##  
    ##  Topic 17, Group 0: donba, eurasian, azerbaijani, turkmenistan, uzbekistan, tashkent, kazakhstan, georgian, silk, belarus, azerbaijan, dniester, turkmenistan’, nistru, nazarbaev, transdniestrian, cica, guuam, aral, dushanb 
    ##  Topic 17, Group 1: zagreb, slovakia, slovak, austria, nature’, minurca, lebanon’, protect”, eurozon, hungari, croatia’, amisom, workshop, khalifa, mohácsi, viktória, baghlan, everyoneí, progress-friend, odccp 
    ##  
    ##  Topic 18, Group 0: caledonian, bougainvill, mururoa, kamises, bougainvillean, tarawa, auckland, distant-water-fish, honiara, moresbi, pccp, ratu, re-inscript, msg, fijian, bamian, waigani, vila, bougainvillian, drift-net 
    ##  Topic 18, Group 1: polaris, mobilis, characteris, non-lebanes, cfc, area-wid, bitterly-divid, confidence·build, worc, guildford, local-author, maguir, mon-prolifer, srian, union», economic-reconstruct, yilmax, yilmaz, fair-employ, keenan 
    ## 

``` r
plot(t0_k18_cont_EU, type = "perspectives", topics = 1)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k18_cont_EU-1.png)

``` r
plot(t0_k18_cont_EU, type = "perspectives", topics = 2)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k18_cont_EU-2.png)

``` r
plot(t0_k18_cont_EU, type = "perspectives", topics = 3)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k18_cont_EU-3.png)

``` r
plot(t0_k18_cont_EU, type = "perspectives", topics = 4)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k18_cont_EU-4.png)

``` r
plot(t0_k18_cont_EU, type = "perspectives", topics = 5)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k18_cont_EU-5.png)

``` r
plot(t0_k18_cont_EU, type = "perspectives", topics = 6)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k18_cont_EU-6.png)

``` r
plot(t0_k18_cont_EU, type = "perspectives", topics = 7)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k18_cont_EU-7.png)

``` r
plot(t0_k18_cont_EU, type = "perspectives", topics = 8)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k18_cont_EU-8.png)

``` r
plot(t0_k18_cont_EU, type = "perspectives", topics = 9)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k18_cont_EU-9.png)

``` r
plot(t0_k18_cont_EU, type = "perspectives", topics = 10)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k18_cont_EU-10.png)

``` r
plot(t0_k18_cont_EU, type = "perspectives", topics = 11)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k18_cont_EU-11.png)

``` r
plot(t0_k18_cont_EU, type = "perspectives", topics = 12)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k18_cont_EU-12.png)

``` r
plot(t0_k18_cont_EU, type = "perspectives", topics = 13)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k18_cont_EU-13.png)

``` r
plot(t0_k18_cont_EU, type = "perspectives", topics = 14)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k18_cont_EU-14.png)

``` r
plot(t0_k18_cont_EU, type = "perspectives", topics = 15)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k18_cont_EU-15.png)

``` r
plot(t0_k18_cont_EU, type = "perspectives", topics = 16)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k18_cont_EU-16.png)

``` r
plot(t0_k18_cont_EU, type = "perspectives", topics = 17)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k18_cont_EU-17.png)

``` r
plot(t0_k18_cont_EU, type = "perspectives", topics = 18)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k18_cont_EU-18.png)

``` r
labelTopics(t0_k18_cont_EU, n = 20)
```

    ## Topic Words:
    ##  Topic 1: kohl, honeck, erich, space-bas, abm, german-polish, helmut, german, responsi¬bl, pan-european, situa¬t, andropov, persh, cmea, states-soviet, con¬tinu, intermediate-rang, honak, ural, good-neighbor 
    ##  Topic 2: l’aquila, johnson-sirleaf, himalayan, rights-bas, cybercrim, climate-resili, att, michell, bachelet, gordon, peacebuild, cyber, -track, childbirth, community-bas, obama’, pittsburgh, busan, arctic, tsunami 
    ##  Topic 3: tit, rumor, egyptian-isra, indo-china—, tween, late—, roger, heng, samrin, vaniti, tion, regime-, brillianc, gromyko, ultima, indochina, seychell, kissing, lndo-china, re-divid 
    ##  Topic 4: tempest, fathom, ungovern, indec, foul, plug, kennedi, thick, shred, glass, tyrant, thunder, roll-cal, sync, scari, metropoli, self-lov, unmoor, yanukovych, spinoza 
    ##  Topic 5: todayâ, rapid-react, cost-cut, “cultur, aconf, unpaid, slavonia, standbi, kinkel, fiftieth-anniversari, high-readi, tribunal’, dual-us, ecosoc, “supplement, anti-personnel, peace-enforc, stand-, secretariat’, robinson 
    ##  Topic 6: staffan, ross, syrian, lakhdar, refugees’, abdulaziz, syria’, daesh, león, syria, nassir, kerri, vuk, respres, al-nass, two-stat, bahraini, abadi, work”, al-abadi 
    ##  Topic 7: marcoussi, kivu, bunia, libérat, fnl, monuc, national, somalian, codesa, inter-congoles, unami, congoles, mouvement, africa-europ, booby-trap, circumcis, eufor, monuc’, artemi, kinshasa 
    ##  Topic 8: peace¬keep, recog¬n, habib, con¬cern, lebanon—, par¬ticular, responsi¬bl, situa¬t, obduraci, israel—, terri¬tori, coun¬tri, interna¬t, governments—, hag, con¬sider, accord¬, con¬tinu, con¬vent, flimsi 
    ##  Topic 9: nkomati, sadcc, imp, contadora, shorter-rang, population—, pan-africanist, gbadolit, south-north, pre-implement, pinié, bophuthatswana, venda, catalog, intermediate-rang, bast, internationalis, ifad, problems—, non-whit 
    ##  Topic 10: chapultepec, minurso, minugua, guatemalteca, unidad, mitch, sfor, hunan, andorra, revolucionaria, reincorpor, urng, “agenda, stabilis, bahía, radicalis, croatian-muslim, long-tem, mallorca, ghali 
    ##  Topic 11: varosha, bizon, ankara, papandreou, famagusta, cypriot, greek, bi-zon, turkish-cypriot, turkey’, turkish, lausann, bi-commun, bicommun, aegean, situation—, turkey, aguirr, greek-turkish, greec 
    ##  Topic 12: nonnuclear, mekong, countries—develop, hartl, scone, -white, hope-giv, slang, number-, commit-, seyn, cut-back, longterm, assis¬t, developed—, war-tim, revitalis, mcnamara, multiyear, aiaddl 
    ##  Topic 13: isil, al-assad’, bashar, dilma, bisexu, transgend, rousseff, history’, gay, synagogu, al-assad, islamist, else’, daesh, clone, stiglitz, third-largest, wake-, beslan, rouhani’ 
    ##  Topic 14: virgilio, argentinean, varga, barco, bradi, amort, wide¬spread, bruntland, felip, lender, tela, refinanc, lopez, portillo, plata, drape, argentina’, solitud, gonzalez, vitoria 
    ##  Topic 15: roger, smack, valeri, gairi, giscard, yaound, latin-american, gaull, spice, guide-lin, desta, us-, underwat, ahidjo, unplan, meetingj, gowon, well-understood, simplic, years- 
    ##  Topic 16: post-independ, chiluba, quota-fre, re-engag, life-sav, scotland, unmil, zimbabwean, baidoa, small-hold, sub-standard, land-min, garang, mahiga, childbirth, darfur, kenyan, ngara, “total, duty-fre 
    ##  Topic 17: romania’, bulgaria’, undcp, romanian, pristina, romania, transdniestria, nations-l, bulgaria, transregion, bratislava, ossetia, ctc, khatami, roma, fukushima, macedonia’, kosovar, karzai, opium 
    ##  Topic 18: chlorofluorocarbon, re-unif, rocard, micronesia, ocean-b, tlatelolco, capitalis, pew, liberalis, reforest, antarctica, ozon, westminst, marshal, minimis, law-mak, tropic, antarct, vessel, chemical-weapon 
    ##  
    ##  Covariate Words:
    ##  Group 0: restructur, legisl, expedit, complet, provis, includ, valuabl, isol, constitut, consult, various, sincer, implement, annal, gracious, date, believ, agreement, taken, initi 
    ##  Group 1: brdo, penalty”, teammat, responsibilities—, ever-recur, eroglu, liais, non-libyan, re-ignit, union-brok, “platform”, anastasiad, lubber, ruud, akıncı, reprofil, dimitri, fourier, intensity”, sophocl 
    ##  
    ##  Topic-Covariate Interactions:
    ##  Topic 1, Group 0: gierek, rapacki, presidium, husak, soviet-indian, soviet-french, songun, anti-reunif, pre-revolutionari, korea-unit, batmunkh, ilyich, politbureau, ceaugescu, tsedenb, freeze”, khural, anti-hitlerit, kosciuszko, parti¬cular 
    ##  Topic 1, Group 1: german-soviet, locomot, ecologically-ori, equalis, good-exampl, hop·, peace-inspir, stability-ori, cooperation—polit, hered, moscow—, punishment—, states—soon, verdun, vmf, aachen, aerosol, economy-ecolog, ícscr, molohi 
    ##  
    ##  Topic 2, Group 0: ldcs, non-communic, tuvalu’, lucia’, redd, reparatori, erika, grenada’, barbuda’, tonga’, oec, bangla, pan-caribbean, dominica’, barbudan, jamaica’, tobago’, jeann, ncds, ldc 
    ##  Topic 2, Group 1: cyberattack, aristotl, vilnius, estonian, estonia, estonia’, latvia, iceland’, lithuania, hammarskjöld, country-own, still-great, donorship, -earth, reverse”, transsexu, near-glob, chaghcharan, man-creat, sea-dump 
    ##  
    ##  Topic 3, Group 0: demarch, kampuchea-thailand, phen, pursat, battambang, awac, second-world, cham, sr-, kaishek, corinto, valparaiso, takeo, walker, hoang, glorieus, sinovietnames, sek, hua, kuo-feng 
    ##  Topic 3, Group 1: gierek, non-inflationari, also-inde, begun-, bremen, germany-berlin, germany-yesterday, liver, midst—solomon, participants-, sessions-, world—quit, cooperation—awar, process—without, secure—, years—doubl, andi, peace-cr, peace-preserv, alonb 
    ##  
    ##  Topic 4, Group 0: disempow, monoth, andorran, andorra’, pyrene, shakespear, saviour, vulgar, camera, smack, painless, vendetta, feather, jewel, belfast, vault, theolog, heresi, cathedr, aristotl 
    ##  Topic 4, Group 1: britain’, cfe, drone, tadeusz, zepa, dermatolog, fifth-centuri, flavius, flood’, hodel, lapland, pradesh, publius, reagan’, renatus’, sunglass, uttar, vegetius, wide-brim, will￼unfortun 
    ##  
    ##  Topic 5, Group 0: iceland’, monaco’, people-smuggl, slovakia, malta’, monaco, dividend”, war-affect, princess, chile’, “renew, reform”, “white, convention’, marino, protect”, unscom, canada’, slovak, nato’ 
    ##  Topic 5, Group 1: greenland, zepa, unamir, kabila’, herzegovina’, non-albanian, tyrol, bosnian, croat, tyrolean, salman, tashkent, untac, unprofor, hutu, forty-eighth, better-defin, ingvar, â€œto, denmarkâ 
    ##  
    ##  Topic 6, Group 0: egypt’, salman, melilla, al-nahyan, emirati, emirates’, al-saud, al-shareef, sa’dah, hadi, derna, tumb, shab’, yemen’, shaikh, mousa, al-shura, oman’, abidin, qaboo 
    ##  Topic 6, Group 1: malta’, boubacar, isi, guinea-bissau’, minsk, valletta, donba, séléka, non-communic, mali, malta, mali’, commission-leagu, marco’, israel-bash, human-rights-protect, political-diplomat, “nurs, diptych, jibreel 
    ##  
    ##  Topic 7, Group 0: séléka, mali’, kabila’, minurca, guinea-bissau’, malian, tutsi, houphouet-boigni, hutu, bangui, ondimba, togo’, senatori, mohéli, ange-félix, patassé, démocrati, inter-burundian, toumani, copax 
    ##  Topic 7, Group 1: unta, eleg, -pronounc, often-understand, shake-, braudel, capitalism, cold-heart, économi, fernand, matériell, lièg, outgam, calculation”, crate, haesendonck, razili, weu’, niass, casino-lik 
    ##  
    ##  Topic 8, Group 0: deir, tiran, jewri, qibya, shatt-al-arab, haaretz, mosh, kafr, khanaqin, barzani, basrah, weizmann, dayan, bani-sadr, shatt-el-arab, defac, judea, qasr-eshirin, fahmi, judaea 
    ##  Topic 8, Group 1: demarch, thai-kampuchean, argentin, africa-, area-includ, country-namibia-, emphasize-, involved-accept, limitations-, limited-posit, odious-, order-even, us-everi, bevin, english-languag, pro-duc, -promis, borrow—, just—world, long-canvass 
    ##  
    ##  Topic 9, Group 0: transkei, -payment, koevoet, traor, administrator-gener, turnhall, siaka, pac, ershad, apper, kountch, supremacist, jayewarden, chad-libya, seyni, carletonvill, afrikan, reed, kolingba, al-hadj 
    ##  Topic 9, Group 1: roh, egyptian-isra, acp-partn, case-fir, community-hungari, ecus, geroayel, h-saharan, institution·, one-point, re-acceler, apvpp-, cpc, frontiers·, hein, piet, plaid, single·, your, conflictand 
    ##  
    ##  Topic 10, Group 0: croatia, non-albanian, herzegovina’, croatia’, latvia, icti, marginalis, guido, croat, serbian, civilis, zagreb, herzegovina, liberalis, unta, lithuania, estonia, croatian, kosova, bosnia 
    ##  Topic 10, Group 1: spain’, gibraltar, spaniard, cplp, melilla, macao, spain, alioun, spanish, portuguese-speak, unita’, cruz, houphouet-boigni, santa, portugues, unita, arbitration-security-disarma, barcelona”, colony’, voter-identif 
    ##  
    ##  Topic 11, Group 0: tyrolean, tyrol, valletta, partitionist, enosi, greek-cypriot, spaniard, ataturk, kemal, state—, rill, ever-escal, austrian, kreiski, euro-mediterranean, austria, lazar, us-, mojsov, short-com 
    ##  Topic 11, Group 1: greece’, casus, islet, pan-american, island’, gambari, fahd, cypriot-own, talat’, “fact”, ciller, gávdhos, greek-bulgarian, ioannina, nesto, varna, cypriot-l, ankara’, clerides’, karpass 
    ##  
    ##  Topic 12, Group 0: roh, ecaf, nepal, arf, yen, bikram, bir, cambodia’, nam’, birendra, yasushi, dev, farakka, tae, wangchuck, nepales, singy, woo, jigm, pattaya 
    ##  Topic 12, Group 1: painless, jewri, antill, self-examin, transkei, allana, export-credit, outbalanc, recover, self-profess, sub-commission—must, assume-, banjak, convention-albeit, government-lik, jia, key-word, nations-tens, objective-, others-observ 
    ##  
    ##  Topic 13, Group 0: drone, chávez, isi, pakistan’, tamil, mohtarma, taliban’, evo, decertifi, ltte, lavala, herat, eelam, lanka’, hizbullah, benazir, kandahar, morazán, libel, raúl 
    ##  Topic 13, Group 1: blanco, feather, greek-cypriot, eisenhow, deir, nafusa, zawiyah, al-sheitaat, campuses”, enemies’, ez-zor, isil”, klansmen, quasi-mediaev, againlf, countrywomen, daraa, happen”, islamist-l, kleptocraci 
    ##  
    ##  Topic 14, Group 0: paz, argentin, brazil’, quito, peruvian, bánzer, lozada, zuazo, quechua, quetzal, belaund, coca-leaf, ecuador’, borja, zamora, peru’, bolivian, garcía, sánchez, portofspain 
    ##  Topic 14, Group 1: marginalis, cowri, migliuolo, needier, us-ussr, hispano-british, newly-recov, archenemi, bartoszewski, import-ori, self-giv, wladyslaw, itr, “hungari, communist-socialist, dumping”, nex, non-pot, “lead, canut 
    ##  
    ##  Topic 15, Group 0: edvard, anti-portugues, jean-bedel, trawler, vietcong, sakiet, dahomey, peron, brooksrandolph, uthant, viet-cong, lamizana, bokassa, unctadj, amphictyon, volta, german-soviet, president--lif, leopoldo, -equip 
    ##  Topic 15, Group 1: tiran, rapacki, caledonian, french-speak, hissein, yen, habr, beew, pie-judg, states-keep, stillwithin, successful-, kite, patience-admir, roza, settled-far, sir-presid, baudouin, debate-among, drama- 
    ##  
    ##  Topic 16, Group 0: amisom, unita’, al-bashir, abyei, renamo, ecomog, eritrean, sadc, unmiss, mkapa, liberia’, machako, badm, somaliaí, ruf, tanzania’, swaziland’, bowen, parpa, ethiopia’ 
    ##  Topic 16, Group 1: belfast, ira, unionist, anglo-irish, ireland, ireland’, obscen, irish, afrikan, decommiss, lankan, bankintern, compliance”, godana, post-lomé, burma’, aiken, lessons-learn, aiken’, rice’ 
    ##  
    ##  Topic 17, Group 0: donba, eurasian, azerbaijani, turkmenistan, uzbekistan, tashkent, kazakhstan, georgian, silk, belarus, azerbaijan, dniester, turkmenistan’, nistru, nazarbaev, transdniestrian, cica, guuam, aral, dushanb 
    ##  Topic 17, Group 1: zagreb, slovakia, slovak, austria, nature’, minurca, lebanon’, protect”, eurozon, hungari, croatia’, amisom, workshop, khalifa, mohácsi, viktória, baghlan, everyoneí, progress-friend, odccp 
    ##  
    ##  Topic 18, Group 0: caledonian, bougainvill, mururoa, kamises, bougainvillean, tarawa, auckland, distant-water-fish, honiara, moresbi, pccp, ratu, re-inscript, msg, fijian, bamian, waigani, vila, bougainvillian, drift-net 
    ##  Topic 18, Group 1: polaris, mobilis, characteris, non-lebanes, cfc, area-wid, bitterly-divid, confidence·build, worc, guildford, local-author, maguir, mon-prolifer, srian, union», economic-reconstruct, yilmax, yilmaz, fair-employ, keenan 
    ## 

``` r
plot(t0_k24_cont_EU, type = "perspectives", topics = 1)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k24_cont_EU-1.png)

``` r
plot(t0_k24_cont_EU, type = "perspectives", topics = 2)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k24_cont_EU-2.png)

``` r
plot(t0_k24_cont_EU, type = "perspectives", topics = 3)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k24_cont_EU-3.png)

``` r
plot(t0_k24_cont_EU, type = "perspectives", topics = 4)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k24_cont_EU-4.png)

``` r
plot(t0_k24_cont_EU, type = "perspectives", topics = 5)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k24_cont_EU-5.png)

``` r
plot(t0_k24_cont_EU, type = "perspectives", topics = 6)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k24_cont_EU-6.png)

``` r
plot(t0_k24_cont_EU, type = "perspectives", topics = 7)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k24_cont_EU-7.png)

``` r
plot(t0_k24_cont_EU, type = "perspectives", topics = 8)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k24_cont_EU-8.png)

``` r
plot(t0_k24_cont_EU, type = "perspectives", topics = 9)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k24_cont_EU-9.png)

``` r
plot(t0_k24_cont_EU, type = "perspectives", topics = 10)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k24_cont_EU-10.png)

``` r
plot(t0_k24_cont_EU, type = "perspectives", topics = 11)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k24_cont_EU-11.png)

``` r
plot(t0_k24_cont_EU, type = "perspectives", topics = 12)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k24_cont_EU-12.png)

``` r
plot(t0_k24_cont_EU, type = "perspectives", topics = 13)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k24_cont_EU-13.png)

``` r
plot(t0_k24_cont_EU, type = "perspectives", topics = 14)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k24_cont_EU-14.png)

``` r
plot(t0_k24_cont_EU, type = "perspectives", topics = 15)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k24_cont_EU-15.png)

``` r
plot(t0_k24_cont_EU, type = "perspectives", topics = 16)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k24_cont_EU-16.png)

``` r
plot(t0_k24_cont_EU, type = "perspectives", topics = 17)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k24_cont_EU-17.png)

``` r
plot(t0_k24_cont_EU, type = "perspectives", topics = 18)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k24_cont_EU-18.png)

``` r
plot(t0_k24_cont_EU, type = "perspectives", topics = 19)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k24_cont_EU-19.png)

``` r
plot(t0_k24_cont_EU, type = "perspectives", topics = 20)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k24_cont_EU-20.png)

``` r
plot(t0_k24_cont_EU, type = "perspectives", topics = 21)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k24_cont_EU-21.png)

``` r
plot(t0_k24_cont_EU, type = "perspectives", topics = 22)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k24_cont_EU-22.png)

``` r
plot(t0_k24_cont_EU, type = "perspectives", topics = 23)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k24_cont_EU-23.png)

``` r
plot(t0_k24_cont_EU, type = "perspectives", topics = 24)
```

![](unga_2017_analysis_files/figure-markdown_github/t0_k24_cont_EU-24.png)

``` r
labelTopics(t10_k12_cont_EU, n = 20)
```

    ## Topic Words:
    ##  Topic 1: indochines, balkan, kampuchean, nonnuclear, declaratori, ether, theater, ronald, imr, good-neighbour, ideologist, chilean, kampuchea, protector, anti-satellit, greec, martial, reunif, countries—, interst 
    ##  Topic 2: rights-bas, peacebuild, climate-resili, system-wid, sixtieth, post-kyoto, low-carbon, girls’, counter-terror, busan, two-stat, nature’, gender, un-women, anti-corrupt, panel’, michell, driver, “implement, union-unit 
    ##  Topic 3: hissein, habr, -armament, shirley, hamilton, gaull, dishonor, ahidjo, guineabissau, gaston, roger, pro-gramm, senghor, sedar, aouzou, mobutu, peoples—, lavish, indo, -tween 
    ##  Topic 4: sirmium, todayâ, baranja, conflict-prevent, undcp, kfor, cost-cut, sfor, rapid-react, romania, tyrol, milosev, secretariat’, unosom, yeltsin, romanian, unprofor, helmets”, turner, serb 
    ##  Topic 5: cplp, unavem, fnl, alioun, monuc, portuguese-speak, libérat, bicess, kivu, independência, união, angolan, somalian, unita’, blondin, national, guinea-bissau, canton, houphouet-boigni, bissau 
    ##  Topic 6: daesh, isil, mistura, al-assad, staffan, levant, isi, extrajudici, shia, qaeda, ii”, lakhdar, “geneva, mh-, africaí, two-stat, rabbani, syria’, abdullah, sixty-ninth 
    ##  Topic 7: arab-israel, denkta, rights-, racialist, scotland, denktash, ploy, disfigur, unifil, el-sadat, reactor, spurious, flo, palestinian-isra, obduraci, intercommun, unficyp, imr, con¬cern, es- 
    ##  Topic 8: semi-manufactur, guineabissau, addl, aaddl, rights-, focal-point, food-stuff, s-vii, mold, states-, connexion, aguirr, seychell, egotist, pro-gramm, postwar, thirty-first, waldheim, sect, root-caus 
    ##  Topic 9: sadcc, bradi, polaris, untag, esquipula, stabilis, tela, shorter-rang, sensitis, botha, jeopardis, liberalis, sadruddin, pio, slow-, debt-servic, gro, harlem, characteris, utilis 
    ##  Topic 10: vent, painless, lash, rod, undilut, joke, pearson, modicum, flinch, marri, writ, contagion, dumbarton, commentari, misunderstood, oak, heav, self-right, mock, chechnya 
    ##  Topic 11: dilma, lehman, rousseff, delano, gdp, ortega, invis, pittsburgh, magna, entrepreneur, oligarchi, uruguayan, reproduc, totalitarian, rodriguez, neoliber, smell, franci, biofuel, espionag 
    ##  Topic 12: duty-fre, trade-distort, collat, dioxid, germany’, unmanag, ireland’, self-help, emiss, gase, typhoon, leaders’, â€”, yeltsin, distil, ogata, “climat, ozon, metr, belfast 
    ##  
    ##  Covariate Words:
    ##  Group 0: allianc, punit, train, curtail, ambassador, carri, plan, sympathi, suspend, rostrum, guarante, prompt, octob, along, locat, washington, harm, lofti, ceas, gracious 
    ##  Group 1: spaak, carrington, der, van, european, initial, remit, ever-clos, kurd, ready-mad, underlin, tuesday, weeks’, reformist, inter-parliamentari, sisyphus, harsher, -site, louis, autumn 
    ##  
    ##  Topic-Covariate Interactions:
    ##  Topic 1, Group 0: andropov, presidium, czechoslovak, erich, jaruzelski, husak, zhivkov, ssr, ilyich, todor, shcherbitski, anti-hitl, jong, ceausescu, byelorussian, binari, byelorussia, anti-soviet, military-strateg, mongolian 
    ##  Topic 1, Group 1: greece’, acqui, ankara, turkey’, unitari, settler, turkish-cypriot, peripher, turkish, null, greek-turkish, obliter, turkey, denktash, bi-commun, zeal, greek, danish, hellen, bizon 
    ##  
    ##  Topic 2, Group 0: ncds, lucia’, tuvalu’, bangabandhu, jamaica’, tonga’, grenada’, sid, tongan, ldc, oec, nepal’, banana-produc, one-size-fits-, ramsi, mongolia’, kitt, barbadian, tobago, samoa’ 
    ##  Topic 2, Group 1: slovakia, latvia’, provinci, slovak, vilnius, latvia, kosovo’, estonian, latvian, georgia’, malta, slovenia, estonia, transdniestria, karzai, malta’, pakistan’, georgian, olmert, maltes 
    ##  
    ##  Topic 3, Group 0: sekou, marien, hoxha, enver, social-imperialist, social-imperi, ngouabi, glorieus, caetano, reconqu, fretilin, independent, sese, libertagao, lon, nol, seko, machiavellian, ratsiraka, kountch 
    ##  Topic 3, Group 1: errat, equilibrium, guide-lin, subservi, latin-american, mururoa, tribul, planetari, hormuz, abort, doubtless, presidium, el-sadat, victor, contagion, alec, disenchant, strait, leonid, plata 
    ##  
    ##  Topic 4, Group 0: nazarbaev, nursultan, turkmenistan’, kuchma, post-confront, aral, albania’, moldovan, bishkek, post-communist, belarus, nagorno-karabakh, eurasian, cica, astana, kyrgyz, ashgabat, nagorny-karabakh, serbia’, armenia’ 
    ##  Topic 4, Group 1: laud, italy’, attun, malici, greenland, maastricht, killer, bangui, crusad, rwanda’, halonen, guyana, france’, blondin, tarja, war-stricken, dougla, cordovez, asean’, spanish 
    ##  
    ##  Topic 5, Group 0: bangui, unamir, jona, mali’, idriss, debi, tutsi, obiang, ondimba, buyoya, ecca, compaoré, mbasogo, ruf, divoir, biya, rwandes, anjouan, burkina, compaor 
    ##  Topic 5, Group 1: merchandis, belgium, cruz, ibero-american, santa, paul-henri, sese, non-self-govern, future”, seko, portugal’, oceanograph, ibero, lisbon, duty-bound, magna, deport, eurasian, paz, portugues 
    ##  
    ##  Topic 6, Group 0: karzai, abidin, sana’, yemen’, sudan’, tumb, sheba’, gcc, eritrean, morocco’, algeria’, zine, pakistan’, ethiopia’, eritrea’, kashmiri, hamad, arta, tunb, musa 
    ##  Topic 6, Group 1: bulgarian, smallhold, bulgaria, bulgaria’, deir, minsk, mali, nefari, -fli, interview, non-communic, gender-bas, ukraine’, patent, diaspora, bisexu, transgend, genit, mali’, man’ 
    ##  
    ##  Topic 7, Group 0: deir, hormuz, non-arab, judea, euphrat, samaria, khomeini, fahd, -fli, ayatollah, hafez, ankara, rejectionist, jew, yassin, iranian, amman, zionist, lebanon’, jordanian 
    ##  Topic 7, Group 1: anglo-irish, belfast, ireland, unionist, irish, inequit, sombr, zeal, republican, argentin, paramilitari, nobli, dublin, co-operation—, rhodesia, ford, thatcher, sat, northern, indomit 
    ##  
    ##  Topic 8, Group 0: unctadj, re-sourc, geostationari, hamilton, shirley, gibraltar, portillo, lopez, country-, gaston, spaniard, tyrol, peace-, uthant, bokassa, corrl, spanish, -selv, guide-lin, boumedien 
    ##  Topic 8, Group 1: erich, andropov, helmut, schmidt, fahd, develop¬, govern¬, sarki, gene, kohl, monstrous, inter-arab, heng, samrin, inflow, medium-rang, bondag, nine, ural, inim 
    ##  
    ##  Topic 9, Group 0: birendra, dev, bir, bikram, koevoet, prise, pac, reed, unban, deflationari, disinvest, rashe, nepal, maldiv, humayun, swaziland, modicum, nepales, cognis, arap 
    ##  Topic 9, Group 1: gibraltar, twelv, spain, spaniard, spanish, argentina’, csce, philippin, duma, belliger, sail, hungarian, glimps, unblock, strangl, basket, mecca, navig, syndrom, declaratori 
    ##  
    ##  Topic 10, Group 0: heresi, astronaut, ltte, unconsci, surgeri, beholden, tamil, theolog, brooksrandolph, roar, whittl, shakespear, saviour, bibl, ugandan, buddhism, sweet, chant, recit, vault 
    ##  Topic 10, Group 1: netherland, unamir, unprofor, cfe, bluff, antill, standbi, refut, rwanda’, duty-bound, nongovernment, us-, surinam, capitalist, bosnian, fraud, australian, ecuador, incess, rwanda 
    ##  
    ##  Topic 11, Group 0: bolivian, brazil’, paraguayan, itaipu, tegucigalpa, inter-ocean, venezuelan, rodrigo, coca, balagu, bolivia’, sucr, evo, amia, cochabamba, juarez, celac, fujimori, ecuador’, saavedra 
    ##  Topic 11, Group 1: poland’, italy’, l’aquila, tadeusz, spaniard, e-govern, itali, onlin, expo, public-priv, italian, zagreb, unitari, france’, illusori, estonia, andor, jeddah, obstin, klaus 
    ##  
    ##  Topic 12, Group 0: niue, polynesia, distant-wat, marshalles, tuna, tokelau, zealand’, noumea, auckland, honiara, fiji’, fijian, majuro, australian, drift-net, trawl, palau’, matignon, bougainvill, australia’ 
    ##  Topic 12, Group 1: jona, kong, treacher, hong, astronom, brazil’, garang, blair, milosev, britain, sudan’, clearanc, cocain, sarajevo, german, germani, agenda”, orphan, sfor, friday 
    ## 

``` r
plot(t10_k12_cont_EU, type = "perspectives", topics = 1)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k12_cont_EU-1.png)

``` r
plot(t10_k12_cont_EU, type = "perspectives", topics = 2)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k12_cont_EU-2.png)

``` r
plot(t10_k12_cont_EU, type = "perspectives", topics = 3)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k12_cont_EU-3.png)

``` r
plot(t10_k12_cont_EU, type = "perspectives", topics = 4)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k12_cont_EU-4.png)

``` r
plot(t10_k12_cont_EU, type = "perspectives", topics = 5)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k12_cont_EU-5.png)

``` r
plot(t10_k12_cont_EU, type = "perspectives", topics = 6)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k12_cont_EU-6.png)

``` r
plot(t10_k12_cont_EU, type = "perspectives", topics = 7)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k12_cont_EU-7.png)

``` r
plot(t10_k12_cont_EU, type = "perspectives", topics = 8)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k12_cont_EU-8.png)

``` r
plot(t10_k12_cont_EU, type = "perspectives", topics = 9)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k12_cont_EU-9.png)

``` r
plot(t10_k12_cont_EU, type = "perspectives", topics = 10)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k12_cont_EU-10.png)

``` r
plot(t10_k12_cont_EU, type = "perspectives", topics = 11)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k12_cont_EU-11.png)

``` r
plot(t10_k12_cont_EU, type = "perspectives", topics = 12)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k12_cont_EU-12.png)

``` r
labelTopics(t10_k18_cont_EU, n = 20)
```

    ## Topic Words:
    ##  Topic 1: demilitaris, balkan, bucharest, pre-war, ideologist, reunif, cypriot, hotspot, junta, reunifi, good-neighbour, high-tech, greec, sen, bulgarian, provoc, dissolut, declaratori, ronald, mediterranean 
    ##  Topic 2: peacebuild, rights-bas, michell, climate-resili, low-carbon, zero-toler, human-induc, post-kyoto, busan, counter-terror, system-wid, icc, fukushima, panel’, quota-fre, tsunami, stand-alon, pittsburgh, scorecard, martiniqu 
    ##  Topic 3: roger, dishonor, africa-, guineabissau, ahidjo, nixon, peoples—, brillianc, sudano-sahelian, organization-, non-oil-export, gaull, disarmament—, amort, ghetto, mayott, knell, kissing, lust, sedar 
    ##  Topic 4: rapid-react, unosom, secretariat’, matériel, anti-personnel, slavonia, mine-clear, ayala, cleansing”, yeltsin, dual-us, minurso, standbi, cost-cut, helmets”, land-min, weu, klaus, clearanc, interlinkag 
    ##  Topic 5: fortiori, kinshasa, knell, congoles, inter-african, kivu, somalian, leopold, zairian, codesa, reforest, mouvement, valeri, sese, seko, egoism, wander, demon, zair, sociolog 
    ##  Topic 6: isil, staffan, daesh, al-assad, mh-, jihadist, levant, isi, boko, behead, extrajudici, movi, lakhdar, shia, qaeda, abdullah, sixty-ninth, mistura, bashar, kutesa 
    ##  Topic 7: devel¬op, israel—, coun¬tri, kittani, interna¬t, habib, ismat, pre-implement, shatila, sabra, situa¬t, unifil, egyptian-isra, neighbor, hollai, fez, thirty-seventh, knesset, thirty-sixth, tyrann 
    ##  Topic 8: cushion, non-oil-export, region—, con¬tinu, deceler, states-soviet, coun¬tri, land-bas, kohl, demilitaris, co-op, co¬oper, longterm, sane, riidig, non-inflationari, citadel, intermediate-rang, medium-rang, indira 
    ##  Topic 9: pro-gramm, pontiff, dissuas, argentina’, aguirr, arra, assembly—, encycl, amerasingh, solitud, jaim, paz, prom, president-elect, lievano, peruvian, ate, unforese, leopoldo, non-european 
    ##  Topic 10: us-, africa-, kissing, unplan, longterm, today-, aadd, guineabissau, organization-, rhodesia, unmitig, mcnamara, addl, four-pow, rhodesian, -mile, racialist, salisburi, svi, nonintervent 
    ##  Topic 11: ibero-american, ibero, michell, right-w, microcredit, uruguayan, alba, ortega, â€”, pittsburgh, teenag, multilingu, re-engin, america’, bachelet, anti-crisi, money-laund, clone, lula, spain’ 
    ##  Topic 12: sharon, obscen, ireland’, duty-fre, smart, “climat, arms-control, fork, deton, sat, licens, beret, test-ban, overseen, timor-lest, nuclear-arm, troop-contribut, reded, submerg, zimbabwean 
    ##  Topic 13: jeopardis, polaris, hest, taif, mecca, industrialis, hormuz, characteris, détent, civilis, mobilis, organis, garba, liberalis, cuellar, utilis, kuwait, gulf, mubarak, arab-isra 
    ##  Topic 14: wand, cockpit, shred, indec, fathom, bus, banker, raft, lection, nuanc, manichean, gentl, admonish, mytholog, burnt, shortcut, thick, nurs, dreamt, peddl 
    ##  Topic 15: pristina, romania, bulgaria’, romanian, bulgarian, hungari, bulgaria, transdniestria, transregion, nations-l, ossetia, croatia’, south-eastern, danub, kosovar, herzegovina’, alba, zagreb, kfor, baranja 
    ##  Topic 16: -fold, dhaka, computer, gdp, duty-fre, pension, trade-distort, telephon, gordon, milk, barrel, phone, fund’, sanit, seamless, pregnanc, buy, pharmaceut, macroeconom, sell 
    ##  Topic 17: cplp, blondin, unavem, bey, fnl, libérat, alioun, portuguese-speak, independência, união, bicess, angolan, brazzavill, unita, guinea-bissau, hipc, monuc, chiluba, unita’, bissau 
    ##  Topic 18: malta’, malta, maltes, euro-mediterranean, barcelona, oceanograph, valletta, mediterranean, littor, libyan, libya, mainland, forty-fifth, seab, agency’, tripoli, euro, hard-won, commonwealth, security-build 
    ##  
    ##  Covariate Words:
    ##  Group 0: select, constitut, extend, includ, signific, expedit, zone, harm, scientif, natur, locat, result, internecin, meet, enshrin, washington, took, current, region, januari 
    ##  Group 1: carrington, ever-clos, european, van, initial, ready-mad, der, sisyphus, enquiri, underlin, remit, chirac, introductori, autumn, harsher, relativ, maltreat, censorship, lenienc, unblock 
    ##  
    ##  Topic-Covariate Interactions:
    ##  Topic 1, Group 0: andropov, erich, presidium, persh, zhivkov, anti-hitl, ilyich, todor, husak, ssr, jaruzelski, shcherbitski, jong, anti-soviet, ceausescu, byelorussian, byelorussia, military-strateg, mongolian, honeck 
    ##  Topic 1, Group 1: greek-turkish, turkey’, bizon, ankara, bicommun, bi-zon, bi-commun, hellen, papandreou, turkish-cypriot, turkey, tirana, neo-liber, greek, turkish, settler, athen, landslid, island’, olymp 
    ##  
    ##  Topic 2, Group 0: tuvalu’, emitt, ncds, pan-caribbean, oec, ldc, grenada’, lucia’, jamaica’, nepal’, sid, banana-produc, maiden, ramsi, taiwan’, bhutanes, barbadian, windward, lead-, pro-poor 
    ##  Topic 2, Group 1: latvia’, finland, colloquium, georgia’, latvian, pakistan’, karzai, iceland’, latvia, kosovo’, lebanon’, sweden, nagorno-karabakh, georgian, chávez, aceh, olmert, mbeki, nagorno, provinci 
    ##  
    ##  Topic 3, Group 0: hoxha, enver, social-imperi, social-imperialist, marien, glorieus, heng, samrin, ngouabi, lon, sekou, independent, nol, libertagao, reconqu, caetano, fretilin, mengistu, amus, vorster 
    ##  Topic 3, Group 1: guide-lin, schumann, aaddl, hissein, habr, yaound, latin-american, thant, mururoa, rahman, presidium, portillo, valeri, mujibur, lopez, slender, leonid, alec, equilibrium, happili 
    ##  
    ##  Topic 4, Group 0: german-speak, latvia’, nazarbaev, turkmenistan’, nursultan, cica, bishkek, kazakhstan’, latvian, aral, semipalatinsk, caspian, belarus, slovakia, latvia, kyrgyz, ashgabat, astana, lyon, kazakhstan 
    ##  Topic 4, Group 1: unamir, de-min, croat, cfa, hutu, serb, colloquium, srebrenica, tutsi, asean’, greenland, macedonian, mogadishu, hebron, sfor, revolucionaria, tiger, number-on, italy’, indo 
    ##  
    ##  Topic 5, Group 0: cfa, habr, hissein, houphouet-boigni, yaound, -armament, kolingba, seyni, eyadema, chad-libya, kountch, ndjamena, mbasogo, gnassingb, biya, obiang, nguema, togoles, traor, hadj 
    ##  Topic 5, Group 1: belgium, inter-congoles, spaak, luxembourg, paul-henri, exposur, invoc, monuc, virgilio, acp, co¬oper, barco, notif, interna¬t, amazon, entrepreneurship, eritrean, ink, paz, pini 
    ##  
    ##  Topic 6, Group 0: pakistan’, karzai, tamil, eelam, lanka’, ltte, kashmiri, uzbek, tajikistan’, uzbekistan’, myanmar’, jammu, myanmar, tajikistan, timor-lest, aung, kyi, suu, opium, inter-tajik 
    ##  Topic 6, Group 1: smallhold, minsk, crimea, deir, thabo, ukrainian, right-w, germany’, tornado, mali, -fli, al-assad’, ukrain, nepad, islamist, climate-chang, bisexu, transgend, gay, bourguiba 
    ##  
    ##  Topic 7, Group 0: deir, euphrat, judea, samaria, khomeini, hafez, -fli, arab-israel, jew, yassin, sharon, moslem, rejectionist, saddam, jewish, sarki, non-arab, iraqi-iranian, jar, zionist 
    ##  Topic 7, Group 1: williamsburg, thai-kampuchean, argentin, kampuchean, duart, thatcher, ireland, anglo-irish, peace-enforc, president-elect, callous, icao, kampuchea, contadora, unionist, nonaggress, com-mun, polish, root-caus, denmark 
    ##  
    ##  Topic 8, Group 0: birendra, williamsburg, dev, bir, bikram, untag, hard-cor, countervail, sadcc, thai-kampuchean, major-pow, shorter-rang, ever-escal, botha, pre-implement, nepal, maldiv, koevoet, debt-servic, pac 
    ##  Topic 8, Group 1: erich, german, andropov, jona, persh, honeck, gene, states-, pariti, baromet, helmut, germani, schmidt, salin, csce, environment-friend, hegemon, feder, ural, egoism 
    ##  
    ##  Topic 9, Group 0: duart, portillo, lopez, ayacucho, inter-ocean, amphictyon, juarez, montevideo, torrijos-cart, alfredo, torrijo, suarez, argentin, balagu, stroessner, ecla, geostationari, ecumen, spaniard, herrera 
    ##  Topic 9, Group 1: itali, italian, german-speak, fahd, lincoln, lester, root-caus, drown, greek-turkish, vientian, sensitis, inter-arab, retard, incis, aloud, pour, maltes, seminar, arthur, south-south 
    ##  
    ##  Topic 10, Group 0: aaddl, thant, schumann, brooksrandolph, aladdl, unctadj, uthant, xxvj, tanaka, states-, defoli, -ever, pro-gramm, randolph, angi, guide-lin, leopoldo, benit, pearc, east- 
    ##  Topic 10, Group 1: netherland, al-bashir, con¬tinu, dutch, surinam, biko, nine, cabinet, inter-arab, antill, arra, sarki, genscher, lago, iaea, plutonium, world—, windhoek, anglo-american, self-reli 
    ##  
    ##  Topic 11, Group 0: cocain, chávez, bolivia’, calderón, peru’, fujimori, coca, colombia’, celac, ecuador’, chile’, unasur, urng, guadalajara, attorney, correa, fmln, marijuana, zelaya, panama’ 
    ##  Topic 11, Group 1: spaniard, gibraltar, l’aquila, klaus, spain, neck, mali’, spanish, kfor, fastest-grow, saharan, bigotri, zagreb, parasit, poland, italy’, len, riyadh, imaginari, blacklist 
    ##  
    ##  Topic 12, Group 0: iceland’, bougainvill, mururoa, drift-net, auckland, honiara, niue, polynesia, noumea, marshalles, tokelau, fiji’, matignon, fijian, trawl, kanak, iceland, melanesian, tuna, distant-wat 
    ##  Topic 12, Group 1: anglo-irish, irish, unionist, mitchel, decommiss, republican, belfast, dublin, “toward, ireland, glass, robinson, tamil, garang, luther, vientian, mogadishu, northern, agenda”, pariti 
    ##  
    ##  Topic 13, Group 0: egypt’, tunisia’, mousa, tumb, abidin, hamad, gcc, al-saud, zine, yemen’, omani, arab-islam, maaouya, tunb, land--peac, al-ahmad, taya, al-sabah, kuwait’, jaber 
    ##  Topic 13, Group 1: sadcc, untag, pedro, debt-servic, shorter-rang, twelv, botha, tela, est, states-soviet, csce, forty-second, gbadolit, esquipula, nkomati, punta, florin, gorbachev, roh, forty-third 
    ##  
    ##  Topic 14, Group 0: saviour, theolog, isaiah, shakespear, heresi, bibl, song, consumer, movi, mose, bag, neck, andorran, rogu, lincoln, jewel, vault, andorra, vultur, camera 
    ##  Topic 14, Group 1: arab-israel, danub, france’, countries-, hong, organization-, cocain, kong, antarct, cfe, dividend, al-qaida, metr, pan, kuwait, inf, nations-, genscher, britain, -exploit 
    ##  
    ##  Topic 15, Group 0: nagorno-karabakh, macedonian, azerbaijani, georgian, azerbaijan, georgia’, marino, armenia, tbilisi, albania’, serbia’, metohija, armenia’, moldovan, azerbaijan’, post-communist, baku, turkey’, abkhaz, ankara 
    ##  Topic 15, Group 1: undcp, slovakia, austria, ecumen, slovak, attorney, amisom, greener, greece’, moham, teacher, juvenil, nuclear-cap, austrian, malici, annapoli, bangui, secretariat’, dividend, country-specif 
    ##  
    ##  Topic 16, Group 0: smallhold, rain-f, bangabandhu, malawi’, ziaur, malawian, -five, cubic, biofuel, rahman, malawi, maiz, mujibur, tonn, gnp, bradi, cetera, quota-fre, burundi’, non-oil 
    ##  Topic 16, Group 1: e-govern, cyber, estonian, cyberspac, estonia, cybercrim, onlin, emitt, priest, entrepreneurship, eurozon, rousseff, lithuanian, thoma, cargo, sweden, dreamt, gender-bas, emiss, napl 
    ##  
    ##  Topic 17, Group 0: inter-congoles, al-bashir, amisom, thabo, mali’, eritrean, ethiopia’, tanzania’, kabbah, liberia’, eritrea’, tejan, unamsil, ruf, nepad, museveni, nigeria’, masir, kivu, kabila 
    ##  Topic 17, Group 1: ibero-american, cruz, ibero, timor-lest, santa, weu, future”, “agenda, paz, euro-mediterranean, houphouet-boigni, lisbon, iraq’, high-readi, non-self-govern, “toward, issa, portugal’, oceanograph, vehement 
    ##  
    ##  Topic 18, Group 0: tonga’, tobago, tongan, ramgoolam, chago, trinidad, mauritian, excis, mauritius, icc, archipelago, colloquium, tonga, caricom, italian, diego, trans-ship, navi, suspect, benghazi 
    ##  Topic 18, Group 1: immigr, moot, decade-long, migrat, ali, rabat, pragu, cabl, treki, hotspot, sixty-fourth, influx, irregular, basin, asylum, stoke, submarin, jan, unhcr, migrant 
    ## 

``` r
plot(t10_k18_cont_EU, type = "perspectives", topics = 1)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k18_cont_EU-1.png)

``` r
plot(t10_k18_cont_EU, type = "perspectives", topics = 2)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k18_cont_EU-2.png)

``` r
plot(t10_k18_cont_EU, type = "perspectives", topics = 3)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k18_cont_EU-3.png)

``` r
plot(t10_k18_cont_EU, type = "perspectives", topics = 4)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k18_cont_EU-4.png)

``` r
plot(t10_k18_cont_EU, type = "perspectives", topics = 5)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k18_cont_EU-5.png)

``` r
plot(t10_k18_cont_EU, type = "perspectives", topics = 6)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k18_cont_EU-6.png)

``` r
plot(t10_k18_cont_EU, type = "perspectives", topics = 7)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k18_cont_EU-7.png)

``` r
plot(t10_k18_cont_EU, type = "perspectives", topics = 8)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k18_cont_EU-8.png)

``` r
plot(t10_k18_cont_EU, type = "perspectives", topics = 9)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k18_cont_EU-9.png)

``` r
plot(t10_k18_cont_EU, type = "perspectives", topics = 10)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k18_cont_EU-10.png)

``` r
plot(t10_k18_cont_EU, type = "perspectives", topics = 11)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k18_cont_EU-11.png)

``` r
plot(t10_k18_cont_EU, type = "perspectives", topics = 12)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k18_cont_EU-12.png)

``` r
plot(t10_k18_cont_EU, type = "perspectives", topics = 13)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k18_cont_EU-13.png)

``` r
plot(t10_k18_cont_EU, type = "perspectives", topics = 14)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k18_cont_EU-14.png)

``` r
plot(t10_k18_cont_EU, type = "perspectives", topics = 15)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k18_cont_EU-15.png)

``` r
plot(t10_k18_cont_EU, type = "perspectives", topics = 16)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k18_cont_EU-16.png)

``` r
plot(t10_k18_cont_EU, type = "perspectives", topics = 17)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k18_cont_EU-17.png)

``` r
plot(t10_k18_cont_EU, type = "perspectives", topics = 18)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k18_cont_EU-18.png)

``` r
labelTopics(t10_k18_cont_EU, n = 20)
```

    ## Topic Words:
    ##  Topic 1: demilitaris, balkan, bucharest, pre-war, ideologist, reunif, cypriot, hotspot, junta, reunifi, good-neighbour, high-tech, greec, sen, bulgarian, provoc, dissolut, declaratori, ronald, mediterranean 
    ##  Topic 2: peacebuild, rights-bas, michell, climate-resili, low-carbon, zero-toler, human-induc, post-kyoto, busan, counter-terror, system-wid, icc, fukushima, panel’, quota-fre, tsunami, stand-alon, pittsburgh, scorecard, martiniqu 
    ##  Topic 3: roger, dishonor, africa-, guineabissau, ahidjo, nixon, peoples—, brillianc, sudano-sahelian, organization-, non-oil-export, gaull, disarmament—, amort, ghetto, mayott, knell, kissing, lust, sedar 
    ##  Topic 4: rapid-react, unosom, secretariat’, matériel, anti-personnel, slavonia, mine-clear, ayala, cleansing”, yeltsin, dual-us, minurso, standbi, cost-cut, helmets”, land-min, weu, klaus, clearanc, interlinkag 
    ##  Topic 5: fortiori, kinshasa, knell, congoles, inter-african, kivu, somalian, leopold, zairian, codesa, reforest, mouvement, valeri, sese, seko, egoism, wander, demon, zair, sociolog 
    ##  Topic 6: isil, staffan, daesh, al-assad, mh-, jihadist, levant, isi, boko, behead, extrajudici, movi, lakhdar, shia, qaeda, abdullah, sixty-ninth, mistura, bashar, kutesa 
    ##  Topic 7: devel¬op, israel—, coun¬tri, kittani, interna¬t, habib, ismat, pre-implement, shatila, sabra, situa¬t, unifil, egyptian-isra, neighbor, hollai, fez, thirty-seventh, knesset, thirty-sixth, tyrann 
    ##  Topic 8: cushion, non-oil-export, region—, con¬tinu, deceler, states-soviet, coun¬tri, land-bas, kohl, demilitaris, co-op, co¬oper, longterm, sane, riidig, non-inflationari, citadel, intermediate-rang, medium-rang, indira 
    ##  Topic 9: pro-gramm, pontiff, dissuas, argentina’, aguirr, arra, assembly—, encycl, amerasingh, solitud, jaim, paz, prom, president-elect, lievano, peruvian, ate, unforese, leopoldo, non-european 
    ##  Topic 10: us-, africa-, kissing, unplan, longterm, today-, aadd, guineabissau, organization-, rhodesia, unmitig, mcnamara, addl, four-pow, rhodesian, -mile, racialist, salisburi, svi, nonintervent 
    ##  Topic 11: ibero-american, ibero, michell, right-w, microcredit, uruguayan, alba, ortega, â€”, pittsburgh, teenag, multilingu, re-engin, america’, bachelet, anti-crisi, money-laund, clone, lula, spain’ 
    ##  Topic 12: sharon, obscen, ireland’, duty-fre, smart, “climat, arms-control, fork, deton, sat, licens, beret, test-ban, overseen, timor-lest, nuclear-arm, troop-contribut, reded, submerg, zimbabwean 
    ##  Topic 13: jeopardis, polaris, hest, taif, mecca, industrialis, hormuz, characteris, détent, civilis, mobilis, organis, garba, liberalis, cuellar, utilis, kuwait, gulf, mubarak, arab-isra 
    ##  Topic 14: wand, cockpit, shred, indec, fathom, bus, banker, raft, lection, nuanc, manichean, gentl, admonish, mytholog, burnt, shortcut, thick, nurs, dreamt, peddl 
    ##  Topic 15: pristina, romania, bulgaria’, romanian, bulgarian, hungari, bulgaria, transdniestria, transregion, nations-l, ossetia, croatia’, south-eastern, danub, kosovar, herzegovina’, alba, zagreb, kfor, baranja 
    ##  Topic 16: -fold, dhaka, computer, gdp, duty-fre, pension, trade-distort, telephon, gordon, milk, barrel, phone, fund’, sanit, seamless, pregnanc, buy, pharmaceut, macroeconom, sell 
    ##  Topic 17: cplp, blondin, unavem, bey, fnl, libérat, alioun, portuguese-speak, independência, união, bicess, angolan, brazzavill, unita, guinea-bissau, hipc, monuc, chiluba, unita’, bissau 
    ##  Topic 18: malta’, malta, maltes, euro-mediterranean, barcelona, oceanograph, valletta, mediterranean, littor, libyan, libya, mainland, forty-fifth, seab, agency’, tripoli, euro, hard-won, commonwealth, security-build 
    ##  
    ##  Covariate Words:
    ##  Group 0: select, constitut, extend, includ, signific, expedit, zone, harm, scientif, natur, locat, result, internecin, meet, enshrin, washington, took, current, region, januari 
    ##  Group 1: carrington, ever-clos, european, van, initial, ready-mad, der, sisyphus, enquiri, underlin, remit, chirac, introductori, autumn, harsher, relativ, maltreat, censorship, lenienc, unblock 
    ##  
    ##  Topic-Covariate Interactions:
    ##  Topic 1, Group 0: andropov, erich, presidium, persh, zhivkov, anti-hitl, ilyich, todor, husak, ssr, jaruzelski, shcherbitski, jong, anti-soviet, ceausescu, byelorussian, byelorussia, military-strateg, mongolian, honeck 
    ##  Topic 1, Group 1: greek-turkish, turkey’, bizon, ankara, bicommun, bi-zon, bi-commun, hellen, papandreou, turkish-cypriot, turkey, tirana, neo-liber, greek, turkish, settler, athen, landslid, island’, olymp 
    ##  
    ##  Topic 2, Group 0: tuvalu’, emitt, ncds, pan-caribbean, oec, ldc, grenada’, lucia’, jamaica’, nepal’, sid, banana-produc, maiden, ramsi, taiwan’, bhutanes, barbadian, windward, lead-, pro-poor 
    ##  Topic 2, Group 1: latvia’, finland, colloquium, georgia’, latvian, pakistan’, karzai, iceland’, latvia, kosovo’, lebanon’, sweden, nagorno-karabakh, georgian, chávez, aceh, olmert, mbeki, nagorno, provinci 
    ##  
    ##  Topic 3, Group 0: hoxha, enver, social-imperi, social-imperialist, marien, glorieus, heng, samrin, ngouabi, lon, sekou, independent, nol, libertagao, reconqu, caetano, fretilin, mengistu, amus, vorster 
    ##  Topic 3, Group 1: guide-lin, schumann, aaddl, hissein, habr, yaound, latin-american, thant, mururoa, rahman, presidium, portillo, valeri, mujibur, lopez, slender, leonid, alec, equilibrium, happili 
    ##  
    ##  Topic 4, Group 0: german-speak, latvia’, nazarbaev, turkmenistan’, nursultan, cica, bishkek, kazakhstan’, latvian, aral, semipalatinsk, caspian, belarus, slovakia, latvia, kyrgyz, ashgabat, astana, lyon, kazakhstan 
    ##  Topic 4, Group 1: unamir, de-min, croat, cfa, hutu, serb, colloquium, srebrenica, tutsi, asean’, greenland, macedonian, mogadishu, hebron, sfor, revolucionaria, tiger, number-on, italy’, indo 
    ##  
    ##  Topic 5, Group 0: cfa, habr, hissein, houphouet-boigni, yaound, -armament, kolingba, seyni, eyadema, chad-libya, kountch, ndjamena, mbasogo, gnassingb, biya, obiang, nguema, togoles, traor, hadj 
    ##  Topic 5, Group 1: belgium, inter-congoles, spaak, luxembourg, paul-henri, exposur, invoc, monuc, virgilio, acp, co¬oper, barco, notif, interna¬t, amazon, entrepreneurship, eritrean, ink, paz, pini 
    ##  
    ##  Topic 6, Group 0: pakistan’, karzai, tamil, eelam, lanka’, ltte, kashmiri, uzbek, tajikistan’, uzbekistan’, myanmar’, jammu, myanmar, tajikistan, timor-lest, aung, kyi, suu, opium, inter-tajik 
    ##  Topic 6, Group 1: smallhold, minsk, crimea, deir, thabo, ukrainian, right-w, germany’, tornado, mali, -fli, al-assad’, ukrain, nepad, islamist, climate-chang, bisexu, transgend, gay, bourguiba 
    ##  
    ##  Topic 7, Group 0: deir, euphrat, judea, samaria, khomeini, hafez, -fli, arab-israel, jew, yassin, sharon, moslem, rejectionist, saddam, jewish, sarki, non-arab, iraqi-iranian, jar, zionist 
    ##  Topic 7, Group 1: williamsburg, thai-kampuchean, argentin, kampuchean, duart, thatcher, ireland, anglo-irish, peace-enforc, president-elect, callous, icao, kampuchea, contadora, unionist, nonaggress, com-mun, polish, root-caus, denmark 
    ##  
    ##  Topic 8, Group 0: birendra, williamsburg, dev, bir, bikram, untag, hard-cor, countervail, sadcc, thai-kampuchean, major-pow, shorter-rang, ever-escal, botha, pre-implement, nepal, maldiv, koevoet, debt-servic, pac 
    ##  Topic 8, Group 1: erich, german, andropov, jona, persh, honeck, gene, states-, pariti, baromet, helmut, germani, schmidt, salin, csce, environment-friend, hegemon, feder, ural, egoism 
    ##  
    ##  Topic 9, Group 0: duart, portillo, lopez, ayacucho, inter-ocean, amphictyon, juarez, montevideo, torrijos-cart, alfredo, torrijo, suarez, argentin, balagu, stroessner, ecla, geostationari, ecumen, spaniard, herrera 
    ##  Topic 9, Group 1: itali, italian, german-speak, fahd, lincoln, lester, root-caus, drown, greek-turkish, vientian, sensitis, inter-arab, retard, incis, aloud, pour, maltes, seminar, arthur, south-south 
    ##  
    ##  Topic 10, Group 0: aaddl, thant, schumann, brooksrandolph, aladdl, unctadj, uthant, xxvj, tanaka, states-, defoli, -ever, pro-gramm, randolph, angi, guide-lin, leopoldo, benit, pearc, east- 
    ##  Topic 10, Group 1: netherland, al-bashir, con¬tinu, dutch, surinam, biko, nine, cabinet, inter-arab, antill, arra, sarki, genscher, lago, iaea, plutonium, world—, windhoek, anglo-american, self-reli 
    ##  
    ##  Topic 11, Group 0: cocain, chávez, bolivia’, calderón, peru’, fujimori, coca, colombia’, celac, ecuador’, chile’, unasur, urng, guadalajara, attorney, correa, fmln, marijuana, zelaya, panama’ 
    ##  Topic 11, Group 1: spaniard, gibraltar, l’aquila, klaus, spain, neck, mali’, spanish, kfor, fastest-grow, saharan, bigotri, zagreb, parasit, poland, italy’, len, riyadh, imaginari, blacklist 
    ##  
    ##  Topic 12, Group 0: iceland’, bougainvill, mururoa, drift-net, auckland, honiara, niue, polynesia, noumea, marshalles, tokelau, fiji’, matignon, fijian, trawl, kanak, iceland, melanesian, tuna, distant-wat 
    ##  Topic 12, Group 1: anglo-irish, irish, unionist, mitchel, decommiss, republican, belfast, dublin, “toward, ireland, glass, robinson, tamil, garang, luther, vientian, mogadishu, northern, agenda”, pariti 
    ##  
    ##  Topic 13, Group 0: egypt’, tunisia’, mousa, tumb, abidin, hamad, gcc, al-saud, zine, yemen’, omani, arab-islam, maaouya, tunb, land--peac, al-ahmad, taya, al-sabah, kuwait’, jaber 
    ##  Topic 13, Group 1: sadcc, untag, pedro, debt-servic, shorter-rang, twelv, botha, tela, est, states-soviet, csce, forty-second, gbadolit, esquipula, nkomati, punta, florin, gorbachev, roh, forty-third 
    ##  
    ##  Topic 14, Group 0: saviour, theolog, isaiah, shakespear, heresi, bibl, song, consumer, movi, mose, bag, neck, andorran, rogu, lincoln, jewel, vault, andorra, vultur, camera 
    ##  Topic 14, Group 1: arab-israel, danub, france’, countries-, hong, organization-, cocain, kong, antarct, cfe, dividend, al-qaida, metr, pan, kuwait, inf, nations-, genscher, britain, -exploit 
    ##  
    ##  Topic 15, Group 0: nagorno-karabakh, macedonian, azerbaijani, georgian, azerbaijan, georgia’, marino, armenia, tbilisi, albania’, serbia’, metohija, armenia’, moldovan, azerbaijan’, post-communist, baku, turkey’, abkhaz, ankara 
    ##  Topic 15, Group 1: undcp, slovakia, austria, ecumen, slovak, attorney, amisom, greener, greece’, moham, teacher, juvenil, nuclear-cap, austrian, malici, annapoli, bangui, secretariat’, dividend, country-specif 
    ##  
    ##  Topic 16, Group 0: smallhold, rain-f, bangabandhu, malawi’, ziaur, malawian, -five, cubic, biofuel, rahman, malawi, maiz, mujibur, tonn, gnp, bradi, cetera, quota-fre, burundi’, non-oil 
    ##  Topic 16, Group 1: e-govern, cyber, estonian, cyberspac, estonia, cybercrim, onlin, emitt, priest, entrepreneurship, eurozon, rousseff, lithuanian, thoma, cargo, sweden, dreamt, gender-bas, emiss, napl 
    ##  
    ##  Topic 17, Group 0: inter-congoles, al-bashir, amisom, thabo, mali’, eritrean, ethiopia’, tanzania’, kabbah, liberia’, eritrea’, tejan, unamsil, ruf, nepad, museveni, nigeria’, masir, kivu, kabila 
    ##  Topic 17, Group 1: ibero-american, cruz, ibero, timor-lest, santa, weu, future”, “agenda, paz, euro-mediterranean, houphouet-boigni, lisbon, iraq’, high-readi, non-self-govern, “toward, issa, portugal’, oceanograph, vehement 
    ##  
    ##  Topic 18, Group 0: tonga’, tobago, tongan, ramgoolam, chago, trinidad, mauritian, excis, mauritius, icc, archipelago, colloquium, tonga, caricom, italian, diego, trans-ship, navi, suspect, benghazi 
    ##  Topic 18, Group 1: immigr, moot, decade-long, migrat, ali, rabat, pragu, cabl, treki, hotspot, sixty-fourth, influx, irregular, basin, asylum, stoke, submarin, jan, unhcr, migrant 
    ## 

``` r
plot(t10_k24_cont_EU, type = "perspectives", topics = 1)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k24_cont_EU-1.png)

``` r
plot(t10_k24_cont_EU, type = "perspectives", topics = 2)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k24_cont_EU-2.png)

``` r
plot(t10_k24_cont_EU, type = "perspectives", topics = 3)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k24_cont_EU-3.png)

``` r
plot(t10_k24_cont_EU, type = "perspectives", topics = 4)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k24_cont_EU-4.png)

``` r
plot(t10_k24_cont_EU, type = "perspectives", topics = 5)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k24_cont_EU-5.png)

``` r
plot(t10_k24_cont_EU, type = "perspectives", topics = 6)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k24_cont_EU-6.png)

``` r
plot(t10_k24_cont_EU, type = "perspectives", topics = 7)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k24_cont_EU-7.png)

``` r
plot(t10_k24_cont_EU, type = "perspectives", topics = 8)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k24_cont_EU-8.png)

``` r
plot(t10_k24_cont_EU, type = "perspectives", topics = 9)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k24_cont_EU-9.png)

``` r
plot(t10_k24_cont_EU, type = "perspectives", topics = 10)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k24_cont_EU-10.png)

``` r
plot(t10_k24_cont_EU, type = "perspectives", topics = 11)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k24_cont_EU-11.png)

``` r
plot(t10_k24_cont_EU, type = "perspectives", topics = 12)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k24_cont_EU-12.png)

``` r
plot(t10_k24_cont_EU, type = "perspectives", topics = 13)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k24_cont_EU-13.png)

``` r
plot(t10_k24_cont_EU, type = "perspectives", topics = 14)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k24_cont_EU-14.png)

``` r
plot(t10_k24_cont_EU, type = "perspectives", topics = 15)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k24_cont_EU-15.png)

``` r
plot(t10_k24_cont_EU, type = "perspectives", topics = 16)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k24_cont_EU-16.png)

``` r
plot(t10_k24_cont_EU, type = "perspectives", topics = 17)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k24_cont_EU-17.png)

``` r
plot(t10_k24_cont_EU, type = "perspectives", topics = 18)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k24_cont_EU-18.png)

``` r
plot(t10_k24_cont_EU, type = "perspectives", topics = 19)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k24_cont_EU-19.png)

``` r
plot(t10_k24_cont_EU, type = "perspectives", topics = 20)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k24_cont_EU-20.png)

``` r
plot(t10_k24_cont_EU, type = "perspectives", topics = 21)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k24_cont_EU-21.png)

``` r
plot(t10_k24_cont_EU, type = "perspectives", topics = 22)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k24_cont_EU-22.png)

``` r
plot(t10_k24_cont_EU, type = "perspectives", topics = 23)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k24_cont_EU-23.png)

``` r
plot(t10_k24_cont_EU, type = "perspectives", topics = 24)
```

![](unga_2017_analysis_files/figure-markdown_github/t10_k24_cont_EU-24.png)

``` r
labelTopics(t20_k12_cont_EU, n = 20)
```

    ## Topic Words:
    ##  Topic 1: intermediate-rang, german, ural, buildup, pan-european, good-neighbor, seven-point, demilitaris, anti-fascist, czechoslovak, shevardnadz, labor, bomber, hegemon, czechoslovakia, states-soviet, moscow, gorbachev, quadripartit, vladivostok 
    ##  Topic 2: sadcc, roh, punta, botha, intermediate-rang, est, untag, shorter-rang, debt-servic, esquipula, williamsburg, utilis, khan, nkomati, extran, kampuchean, concession, contadora, tela, non-whit 
    ##  Topic 3: transkei, kissing, biko, rhodesia, rancor, gaston, connexion, waldheim, roger, salisburi, thirty-first, s-vii, flimsi, seychell, labor, mojsov, mekong, kittani, thirty-second, hie 
    ##  Topic 4: unprofor, unosom, ayala, yeltsin, secretariat’, forty-eighth, cleansing”, untac, “ethnic, sarajevo, peace-build, boutros-ghali, bosnian, stand-, kurd, serb, croat, csce, marino, rwanda 
    ##  Topic 5: ankara, turkey’, bi-zon, bizon, turkish, jihad, turkey, cypriot, bicommun, settler, greek, afghani, bi-commun, greec, iraq-kuwait, abdulaziz, airspac, palestine’, cyprus, birthplac 
    ##  Topic 6: driver, peacebuild, low-carbon, obama’, pittsburgh, two-stat, post-kyoto, darfur, gender, un-women, tsunami, arctic, post-, bachelet, rule-bas, phone, system-wid, holist, aung, kyi 
    ##  Topic 7: quota-fre, unrepres, republican, zimbabwean, power-shar, blair, botswana, callous, kiribati, martin, robinson, reded, gratuit, cheaper, bedevil, holkeri, long-run, descent, intract, decim 
    ##  Topic 8: pedro, liberalis, tela, abraham, aziz, gbadolit, sudano-sahelian, fahd, taif, labori, marginalis, civilis, redefinit, guido, sahraoui, characteris, indissolubl, industrialis, democratis, rediscov 
    ##  Topic 9: al-assad, isil, daesh, bashar, privaci, qaeda, behead, wake-, internet, haram, crimea, al-qadhafi, boko, levant, isi, al-qaida, borderless, tyrant, hama, priest 
    ##  Topic 10: slovakia, slovak, dayton, landmin, â€”, downsiz, kosovo, secretariat’, conflict-prevent, anti-personnel, ctbt, fifty-first, post-conflict, romania, osc, peace-build, synergi, fissil, demin, academia 
    ##  Topic 11: countries-, plata, kissing, specious, obsolesc, thant, realpolitik, simplic, nixon, unhappili, inter-depend, angel, adrift, disarray, non-renew, hambro, planetari, peke, oil-produc, quotat 
    ##  Topic 12: ibero-american, gibraltar, spanish, spain, paz, portuguese-speak, america’, ortega, josé, angel, revolucionaria, bachelet, microcredit, antonio, bogota, farabundo, anti-terrorist, nacion, uruguayan, bicess 
    ##  
    ##  Covariate Words:
    ##  Group 0: pocket, scheme, launch, punit, consult, octob, optimist, germ, full, decis, incomplet, regardless, countri, attain, restructur, contain, result, collect, requir, tranquil 
    ##  Group 1: autumn, van, european, centenni, maltreat, unblock, harsher, colleagu, censorship, inward, underlin, outward, madrid, weekend, unsaf, everyday, nutshel, israeli-palestinian, -site, europ 
    ##  
    ##  Topic-Covariate Interactions:
    ##  Topic 1, Group 0: presidium, binari, ssr, jong, byelorussian, soviet-unit, mongolian, andrei, -european, leninist, counterrevolutionari, viet-nam, romania, ussr, romanian, leonid, ukrainian, viet-names, albania, lenin 
    ##  Topic 1, Group 1: semi-manufactur, jona, agit, hardwar, poster, aberr, epoch, food-stuff, self-help, counten, free-market, dar, julius, nest, csce, inim, unfpa, livestock, non-oil, precept 
    ##  
    ##  Topic 2, Group 0: singy, nepal, jigm, wangchuck, saarc, maldiv, jawaharl, archipelag, caledonia, lankan, pac, kanak, surinam, malaysia, samdech, intifadah, garba, bhutto, colombo, non-nuclear-weapon 
    ##  Topic 2, Group 1: kong, hong, twelv, denmark, danish, desol, csce, churchil, ten, navig, implor, chilean, aviat, belliger, purport, cuban, kurdish, nake, pol, -stand 
    ##  
    ##  Topic 3, Group 0: fretilin, lon, vorster, nol, machiavellian, reconquest, turnhall, independencia, houari, paigc, ahgr, partido, zionist, yanke, bassa, lackey, penh, phnom, imperialist, mao 
    ##  Topic 3, Group 1: netherland, aadd, nine, presidium, acrimoni, belgium, acp, precept, sect, happili, belgian, transgress, four-pow, plutonium, iaea, leonid, non-nuclear, time-t, world-wid, pessimist 
    ##  
    ##  Topic 4, Group 0: estonian, georgia’, georgian, malta, kosovo, pristina, serbia, iceland, macedonian, samir, zealand, shihabi, kosovo’, austrian, albanian, albania, latvia, canadian, dayton, abkhazia 
    ##  Topic 4, Group 1: al-bashir, unconscion, palac, tiger, standbi, repar, rapid-react, mismanag, brazil’, refresh, glass, outpour, lawyer, brigad, mogadishu, fraud, co-chairmanship, anti-personnel, tajikistan, builder 
    ##  
    ##  Topic 5, Group 0: deir, egypt’, gcc, bekaa, land--peac, tunb, lebanon’, yemen’, emir, nagorno, azerbaijan’, azerbaijani, hamad, syrian, iranian, yemen, yemeni, hashemit, mosqu, abu 
    ##  Topic 5, Group 1: ronald, tandem, moon, pristina, mainland, olymp, macedonia, quito, landslid, win-win, south-eastern, tourism, plethora, spillov, hydrocarbon, secessionist, athlet, albanian, citizenship, subvert 
    ##  
    ##  Topic 6, Group 0: unreport, ncds, sid, aosi, ldc, acidif, fiji’, coral, fijian, sea-level, kitt, taiwan’, tuna, caricom, montserrat, polynesia, tobago, barbado, guinea’, samoa 
    ##  Topic 6, Group 1: estonian, malta, georgia’, nagorno, latvia, lebanon’, bulgaria, estonia, finland, repuls, gay, georgian, czech, iran’, lithuania, slovenia, ukraine’, maltes, afghanistan’, croatia 
    ##  
    ##  Topic 7, Group 0: al-bashir, inter-congoles, jona, burundi, ecomog, burundian, swazi, leonean, igad, ecowa, ethiopia’, kivu, eritrean, sierra, liberian, taylor, idriss, mano, gambian, malawi 
    ##  Topic 7, Group 1: ireland, unionist, irish, etho, bed, indomit, obscen, decommiss, invalid, falkland, britain, luther, northern, sombr, argentin, temper, trillion, british, ploy, nationalist 
    ##  
    ##  Topic 8, Group 0: malian, biya, eyadema, abidin, togoles, senegales, togo, zine, mauritanian, anjouan, diouf, niger, cameroon, mali, comorian, chadian, benin, ndjamena, burkina, faso 
    ##  Topic 8, Group 1: itali, italian, nations—, extort, restitut, panorama, strangl, argentina’, warship, maltes, naiv, amelior, germ, chaotic, incis, seoul, moro, guilt, non-self-govern, malta 
    ##  
    ##  Topic 9, Group 0: kashmiri, jesus, america’, tamil, tiger, bibl, abraham, pakistan’, allah, jihad, buddha, bag, theolog, consumer, grenad, koran, bhutto, putin, song, divin 
    ##  Topic 9, Group 1: deir, feat, geolog, diabet, egypt’, britain, bereft, belarus, burundian, climate-chang, outstrip, minsk, nepad, bulgarian, kyoto, doha, yemen, nake, umbrella, protect” 
    ##  
    ##  Topic 10, Group 0: kazakhstan, belarus, aral, kyrgyz, turkmenistan, tajikistan, cis, tajik, myanmar’, uzbekistan, semipalatinsk, azerbaijan, moldova, caspian, armenia, kyrgyzstan, ticad, reform”, “renew, minsk 
    ##  Topic 10, Group 1: austria, hungari, austrian, pristina, provinci, monuc, juvenil, seminar, romanian, serb, tyrol, hungarian, ahtisaari, sierra, sweden, swedish, moham, sacrosanct, taliban, leon 
    ##  
    ##  Topic 11, Group 0: volta, food-stuff, leopoldo, rancor, uthant, re-sourc, semi-manufactur, addl, geolog, unctadj, undevelop, theolog, sea-b, gaston, waldheim, labor, niue, hie, thorn, kurt 
    ##  Topic 11, Group 1: franc, subservi, flora, punit, france’, aristid, slander, chaotic, inter-african, mayor, cannon, refresh, belgium, thai, typhoon, armour, french, notif, pranc, strait 
    ##  
    ##  Topic 12, Group 0: peruvian, rica, costa, paraguay, montevideo, inter-ocean, coca, brazil’, paraguayan, tegucigalpa, bolivian, quito, ecuadorian, guatemalan, domingo, honduran, torrijo, rafael, salvadoran, argentin 
    ##  Topic 12, Group 1: kivu, angolan, timores, monuc, portugues, mirag, belgium, future”, inter-congoles, portug, unita, non-self-govern, crux, subvert, congoles, luxembourg, belgian, park, guinea-bissau, didier 
    ## 

``` r
plot(t20_k12_cont_EU, type = "perspectives", topics = 1)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k12_cont_EU-1.png)

``` r
plot(t20_k12_cont_EU, type = "perspectives", topics = 2)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k12_cont_EU-2.png)

``` r
plot(t20_k12_cont_EU, type = "perspectives", topics = 3)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k12_cont_EU-3.png)

``` r
plot(t20_k12_cont_EU, type = "perspectives", topics = 4)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k12_cont_EU-4.png)

``` r
plot(t20_k12_cont_EU, type = "perspectives", topics = 5)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k12_cont_EU-5.png)

``` r
plot(t20_k12_cont_EU, type = "perspectives", topics = 6)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k12_cont_EU-6.png)

``` r
plot(t20_k12_cont_EU, type = "perspectives", topics = 7)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k12_cont_EU-7.png)

``` r
plot(t20_k12_cont_EU, type = "perspectives", topics = 8)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k12_cont_EU-8.png)

``` r
plot(t20_k12_cont_EU, type = "perspectives", topics = 9)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k12_cont_EU-9.png)

``` r
plot(t20_k12_cont_EU, type = "perspectives", topics = 10)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k12_cont_EU-10.png)

``` r
plot(t20_k12_cont_EU, type = "perspectives", topics = 11)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k12_cont_EU-11.png)

``` r
plot(t20_k12_cont_EU, type = "perspectives", topics = 12)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k12_cont_EU-12.png)

``` r
labelTopics(t20_k18_cont_EU, n = 20)
```

    ## Topic Words:
    ##  Topic 1: german, pan-european, anti-fascist, intermediate-rang, ural, quadripartit, reykjavik, good-neighbor, hegemon, states-soviet, seven-point, postul, czechoslovak, switch, polish, czechoslovakia, moscow, unalter, long-cherish, vladivostok 
    ##  Topic 2: marginalis, untag, ploughshar, export-ori, concession, burmes, creditor, debt, growth-ori, deforest, upturn, stabilis, flower, output, grotesqu, protection, indebt, hazard, burma, plenipotentiari 
    ##  Topic 3: senghor, kissing, root-caus, gaston, short-com, transkei, hie, connexion, food-stuff, s-vl, leopoldo, hambro, seychell, lust, thirty-first, shirley, hamilton, mayott, amerasingh, biko 
    ##  Topic 4: estonia, estonian, secretariat’, peace-build, ayala, baltic, land-min, peace-keep, post-cold-war, stuck, stand-, mouth, robinson, intra-st, test-ban, yeltsin, viii, icrc, willi, peacemak 
    ##  Topic 5: ankara, turkey’, turkish, bi-zon, bi-commun, cypriot, bizon, greek, turkey, bicommun, greec, makario, settler, athen, jet, cyprus, ismat, taif, pre-, shrine 
    ##  Topic 6: michell, rules-bas, “geneva, pittsburgh, phone, un-women, driver, ii”, low-carbon, tsunami, girl, gender, smart, want”, ki-moon, khalifa, digit, second-largest, two-stat, mdgs 
    ##  Topic 7: unrepres, slow-, anc, callous, lull, non-whit, malais, falkland, statesmanship, power-shar, long-run, ploy, appeas, withhold, intract, franchis, long-delay, output, outliv, incurs 
    ##  Topic 8: abraham, fahd, somalia’, mediterranean, el-sheikh, taif, sharm, aziz, barcelona, arabian, paz, damascus, moro, besieg, hotb, thi, righteous, martyr, yoke, confisc 
    ##  Topic 9: gentl, smash, unrepres, sordid, eschew, icrc, muscl, templ, valley, spurn, non-nuclear, plain, hijack, anti-ballist, gloom, rebuff, statesmanship, sanctuari, disposit, non-nuclear-weapon 
    ##  Topic 10: “agenda, test-ban, businesslik, human-resourc, cost-effect, arctic, undp, battalion, non-nuclear-weapon, non-nuclear, iaea, -secretary-gener, troop-contribut, forty-seventh, standard-set, copenhagen, unep, weapon-fre, sofia, step--step 
    ##  Topic 11: countries-, pearson, plata, fantast, kissing, adrift, inter-depend, less-develop, simplic, amort, stanislaw, yalta, precaut, riparian, medit, disarray, lopez, countries—, unhappili, jurist 
    ##  Topic 12: gibraltar, ibero-american, spanish, america’, spain, paz, microcredit, portuguese-speak, revolucionaria, bogota, ortega, argentina’, biennium, josé, uruguayan, asymmetri, multilingu, cartagena, marxist, exponenti 
    ##  Topic 13: extrajudici, “respons, monterrey, system-wid, freedom”, protect”, “develop, mello, ping, sergio, katrina, vieira, thabo, monuc, six-parti, beslan, cologn, icc, quartet, anti-corrupt 
    ##  Topic 14: aung, kyi, suu, obscen, sharon, smart, zimbabwean, ireland, timor, irish, licens, oversea, timor-lest, duty-fre, recommit, reded, netanyahu, poll, countermeasur, downturn 
    ##  Topic 15: romania, pristina, bulgaria, bulgarian, romanian, euro-mediterranean, croatia, south-eastern, transatlant, orthodox, hungari, hungarian, tyrol, dayton, essi, serbian, albanian, euro-atlant, albania, osc 
    ##  Topic 16: coun¬tri, southwest, inter¬n, williamsburg, kittani, northsouth, justice-lov, wechmar, vanuatu, grenadin, salim, thirty-sixth, nonalign, secretarygener, countries—, thirty-seventh, indochines, vincent, superpow, von 
    ##  Topic 17: tela, pitiless, norodom, anc, liberalis, sudano-sahelian, gbadolit, sahraoui, sociolog, reykjavik, jeopardis, mobilis, debt-serv, characteris, maghreb, slow-, deforest, french-speak, major-gener, bean 
    ##  Topic 18: isil, bashar, al-assad, europe’, levant, al-qaida, fractur, crimea, shout, tore, borderless, al-qadhafi, behead, mogen, damascus, buddhist, sleep, haram, second-largest, imam 
    ##  
    ##  Covariate Words:
    ##  Group 0: consult, expedit, decemb, signifi, zone, support, facil, due, implement, issu, outstand, similar, along, enshrin, overwhelm, realiz, inculc, provid, person, extend 
    ##  Group 1: centenni, european, autumn, van, maltreat, censorship, harsher, underlin, nutshel, inward, colleagu, unblock, weekend, unsaf, stricter, everyday, liaison, outward, penalti, appal 
    ##  
    ##  Topic-Covariate Interactions:
    ##  Topic 1, Group 0: presidium, ssr, binari, jong, byelorussian, soviet-unit, leninist, leonid, anti-satellit, ussr, mongolian, lenin, ukrainian, soviet-american, romanian, romania, bulgarian, -european, neutron, viet-nam 
    ##  Topic 1, Group 1: semi-manufactur, jona, transatlant, food-stuff, riidig, dar, nagorno-karabakh, csce, land-lock, aberr, debt-serv, egoism, nigerian, free-market, genet, poster, realis, steal, factori, expuls 
    ##  
    ##  Topic 2, Group 0: liberalis, jeopardis, bradi, revitalis, destabilis, forty-third, intermediate-rang, garba, debt-servic, forty-fourth, utilis, slow-, shorter-rang, characteris, singy, florin, tela, nepal, industrialis, est 
    ##  Topic 2, Group 1: czech, poland, renamo, lyon, wto, communism, kong, sell, bank’, triad, polish, hong, privat, czechoslovakia, rejuven, entrepreneurship, countries’, britain, internet, macroeconom 
    ##  
    ##  Topic 3, Group 0: vorster, reconquest, independencia, houari, somoza, yanke, fretilin, paigc, zimbabwean, zionist, bassa, lackey, agostinho, albania, albanian, saigon, imperialist, turnhall, mauber, mpla 
    ##  Topic 3, Group 1: belgium, leonid, rahman, presidium, acp, belgian, kinshasa, aadd, nine, precept, reproach, phnom, brezhnev, oil-export, happili, degener, dispassion, anguish, retir, wanton 
    ##  
    ##  Topic 4, Group 0: iceland, pearson, latvia, finnish, finland, canadian, norwegian, swedish, liechtenstein, aaddl, lithuania, nordic, reykjavik, canada, lester, unionist, wilson, angi, simplic, arctic 
    ##  Topic 4, Group 1: rapid-react, unprofor, cleansing”, “ethnic, forty-eighth, bosnian, unosom, sarajevo, untac, al-bashir, croat, chechnya, standbi, thunder, pernici, indo, serb, boutros-ghali, bosnia, cis 
    ##  
    ##  Topic 5, Group 0: nagorno, deir, azerbaijani, shatila, sabra, azerbaijan’, azerbaijan, nagorno-karabakh, saddam, karabakh, sharon, iranian, nagorni, tripoli, armenia, lebanes, flimsi, zionist, beirut, iraqi 
    ##  Topic 5, Group 1: landslid, quito, balkan, methodolog, hydrocarbon, win-win, ali, plethora, shelf, skew, jihad, uninhabit, anachronist, “bring, sixty-sixth, catalyt, neighbourhood, frent, â€”, nassir 
    ##  
    ##  Topic 6, Group 0: ncds, acidif, unreport, sid, diabet, kitt, coral, ldc, caricom, taiwan’, montserrat, ldcs, aosi, barbado, dominica, rainforest, abdussalam, geotherm, tobago, mogen 
    ##  Topic 6, Group 1: nagorno, kosovo’, crimea, georgian, pakistan’, malta, ukraine’, gay, malian, afghanistan’, latvia, finland, minsk, russia’, nagorno-karabakh, mali, slovenia, georgia, ossetia, iran’ 
    ##  
    ##  Topic 7, Group 0: al-bashir, eritrean, somalia’, ecomog, ethiopia’, igad, leonean, nigerian, gambian, taylor, igadd, mogadishu, sadc, ethiopian, arap, renamo, liberian, mano, thabo, moi 
    ##  Topic 7, Group 1: unionist, ireland, irish, disinherit, northern, etho, sombr, nation-st, test-ban, major-gener, kuala, lumpur, precept, submarin, unifil, republican, purport, wartim, samir, nationalist 
    ##  
    ##  Topic 8, Group 0: egypt’, hebron, yemen’, land--peac, gcc, tunb, abidin, yemen, zine, hamad, sultan, emir, hashemit, kuwait’, yemeni, musa, abu, tunisia, saleh, maghreb 
    ##  Topic 8, Group 1: itali, italian, maltes, aguirr, malta, encycl, retard, seminar, peruvian, helicopt, incis, south-south, frelimo, community—, equilibrium, defenseless, suffrag, degener, illusori, fatherland 
    ##  
    ##  Topic 9, Group 0: taliban, lankan, pakistan’, rahman, tamil, kabul, kashmir, kashmiri, saarc, afghanistan’, jammu, bhutto, pakistan, rajiv, pakistani, india’, jawaharl, simla, islamabad, bandaranaik 
    ##  Topic 9, Group 1: argentin, falkland, britain, chissano, cocain, venezuelan, lenin, unprovok, antarct, meat, colombian, churchil, rhodesia, zimbabwean, salisburi, british, gorbachev, sail, argentina, botswana 
    ##  
    ##  Topic 10, Group 0: ukraine’, cis, belarus, freita, amar, diogo, aral, kyrgyz, kazakhstan, semipalatinsk, turkmenistan, kyrgyzstan, “renew, reform”, tajikistan, caspian, uzbekistan, demin, razali, amara 
    ##  Topic 10, Group 1: netherland, danish, denmark, nordic, macedonian, dutch, surinam, longterm, sect, covert, biko, revitalis, secretarygener, supervisori, chairperson, corner-ston, hugo, till, condon, tree 
    ##  
    ##  Topic 11, Group 0: volta, food-stuff, rancor, leopoldo, undevelop, semi-manufactur, specious, re-sourc, unctadj, disinherit, geolog, santiago, oil-export, gaston, theolog, malik, hie, hambro, uthant, pauper 
    ##  Topic 11, Group 1: franc, music, anti-satellit, arthur, subservi, smash, fauna, pen, french, demis, punit, gallant, thai, ozon, abort, domain, clear-sight, warhead, antarctica, nurs 
    ##  
    ##  Topic 12, Group 0: peruvian, isthmus, argentin, venezuelan, andean, inter-ocean, paraguay, colombian, montevideo, costa, rica, domingo, guatemalan, paraguayan, quito, salvadoran, coca, rafael, bolivian, tegucigalpa 
    ##  Topic 12, Group 1: portugues, unita, belgium, specious, ghali, timores, didier, portug, lisbon, timor, timor-lest, angolan, maghreb, “agenda, guinea-bissau, chissano, bicess, mozambican, belgian, congoles 
    ##  
    ##  Topic 13, Group 0: sahelo-saharan, ex-combat, ticad, microcredit, francophoni, ezulwini, means”, theo-ben, sixty-sixth, kathmandu, stakehold, burundian, reappoint, nepales, mdgs, deiss, “bring, almati, al-nass, sixty-seventh 
    ##  Topic 13, Group 1: slovakia, austria, slovak, tanzanian, curriculum, islamabad, ctbt, austrian, taliban, seminar, soft, luxembourg, lebanon’, swedish, opium, ahtisaari, post-kyoto, juvenil, npt, ecomog 
    ##  
    ##  Topic 14, Group 0: mururoa, tokelau, fijian, fiji’, niue, polynesia, distant-wat, melanesian, swazi, matignon, tuna, australia’, kanak, atol, fiji, australian, low-li, bougainvill, swaziland, malawi 
    ##  Topic 14, Group 1: lankan, unionist, decommiss, blair, mitchel, tamil, pernici, gay, cluster, buddhist, union-unit, mouth, somalia’, wretch, munit, weep, republican, seattl, agenda”, darfur 
    ##  
    ##  Topic 15, Group 0: macedonian, kosovo’, forty-eighth, samir, csce, malta, croat, unprofor, untac, czech, nagorno-karabakh, boutros-ghali, maltes, cleansing”, yeltsin, “ethnic, gay, eurasia, andorra, austria 
    ##  Topic 15, Group 1: hebron, sacrosanct, francophoni, bangui, abdussalam, â€”, lebanon’, bongo, sheikha, eurasian, al-khalifa, -inclus, ukraine’, cordovez, truce, haya, redeploy, video, landmin, nagorni 
    ##  
    ##  Topic 16, Group 0: phnom, penh, thai, hanoi, vientian, nol, indo, riidig, thailand, lao, minh, samdech, khmer, chi, roug, buddhist, indo-chines, eight-point, lon, laotian 
    ##  Topic 16, Group 1: shatila, sabra, flimsi, disband, non-whit, anti-satellit, rancor, lome, security-build, -stand, polish, covert, thorn, long-rang, dismal, lesotho, ten, sahelian, xxx, non-oil-produc 
    ##  
    ##  Topic 17, Group 0: kinshasa, bangui, bongo, kivu, eyadema, hadj, ndjamena, biya, idriss, togoles, anjouan, mbasogo, senegales, nguema, niger, sassou, nguesso, burkina, togo, abdou 
    ##  Topic 17, Group 1: bradi, twelv, utilis, est, debt-servic, roh, mururoa, destabilis, roug, sadcc, punta, del, pedro, mecca, shorter-rang, sharpevill, isthmus, states-soviet, gorbachev, csce 
    ##  
    ##  Topic 18, Group 0: bibl, georgian, andorra, abraham, america’, music, jesus, shakespear, bag, consumer, theolog, hebrew, song, thunder, castro, chávez, rogu, post-soviet, allah, lula 
    ##  Topic 18, Group 1: diabet, deir, kingdom’, egypt’, geolog, burundian, afghanistan’, belarus, public-priv, minsk, abdullah, umbrella, paus, taliban, france’, protect”, faso, burkina, tribe, yemen 
    ## 

``` r
plot(t20_k18_cont_EU, type = "perspectives", topics = 1)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k18_cont_EU-1.png)

``` r
plot(t20_k18_cont_EU, type = "perspectives", topics = 2)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k18_cont_EU-2.png)

``` r
plot(t20_k18_cont_EU, type = "perspectives", topics = 3)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k18_cont_EU-3.png)

``` r
plot(t20_k18_cont_EU, type = "perspectives", topics = 4)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k18_cont_EU-4.png)

``` r
plot(t20_k18_cont_EU, type = "perspectives", topics = 5)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k18_cont_EU-5.png)

``` r
plot(t20_k18_cont_EU, type = "perspectives", topics = 6)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k18_cont_EU-6.png)

``` r
plot(t20_k18_cont_EU, type = "perspectives", topics = 7)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k18_cont_EU-7.png)

``` r
plot(t20_k18_cont_EU, type = "perspectives", topics = 8)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k18_cont_EU-8.png)

``` r
plot(t20_k18_cont_EU, type = "perspectives", topics = 9)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k18_cont_EU-9.png)

``` r
plot(t20_k18_cont_EU, type = "perspectives", topics = 10)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k18_cont_EU-10.png)

``` r
plot(t20_k18_cont_EU, type = "perspectives", topics = 11)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k18_cont_EU-11.png)

``` r
plot(t20_k18_cont_EU, type = "perspectives", topics = 12)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k18_cont_EU-12.png)

``` r
plot(t20_k18_cont_EU, type = "perspectives", topics = 13)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k18_cont_EU-13.png)

``` r
plot(t20_k18_cont_EU, type = "perspectives", topics = 14)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k18_cont_EU-14.png)

``` r
plot(t20_k18_cont_EU, type = "perspectives", topics = 15)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k18_cont_EU-15.png)

``` r
plot(t20_k18_cont_EU, type = "perspectives", topics = 16)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k18_cont_EU-16.png)

``` r
plot(t20_k18_cont_EU, type = "perspectives", topics = 17)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k18_cont_EU-17.png)

``` r
plot(t20_k18_cont_EU, type = "perspectives", topics = 18)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k18_cont_EU-18.png)

``` r
labelTopics(t20_k18_cont_EU, n = 20)
```

    ## Topic Words:
    ##  Topic 1: german, pan-european, anti-fascist, intermediate-rang, ural, quadripartit, reykjavik, good-neighbor, hegemon, states-soviet, seven-point, postul, czechoslovak, switch, polish, czechoslovakia, moscow, unalter, long-cherish, vladivostok 
    ##  Topic 2: marginalis, untag, ploughshar, export-ori, concession, burmes, creditor, debt, growth-ori, deforest, upturn, stabilis, flower, output, grotesqu, protection, indebt, hazard, burma, plenipotentiari 
    ##  Topic 3: senghor, kissing, root-caus, gaston, short-com, transkei, hie, connexion, food-stuff, s-vl, leopoldo, hambro, seychell, lust, thirty-first, shirley, hamilton, mayott, amerasingh, biko 
    ##  Topic 4: estonia, estonian, secretariat’, peace-build, ayala, baltic, land-min, peace-keep, post-cold-war, stuck, stand-, mouth, robinson, intra-st, test-ban, yeltsin, viii, icrc, willi, peacemak 
    ##  Topic 5: ankara, turkey’, turkish, bi-zon, bi-commun, cypriot, bizon, greek, turkey, bicommun, greec, makario, settler, athen, jet, cyprus, ismat, taif, pre-, shrine 
    ##  Topic 6: michell, rules-bas, “geneva, pittsburgh, phone, un-women, driver, ii”, low-carbon, tsunami, girl, gender, smart, want”, ki-moon, khalifa, digit, second-largest, two-stat, mdgs 
    ##  Topic 7: unrepres, slow-, anc, callous, lull, non-whit, malais, falkland, statesmanship, power-shar, long-run, ploy, appeas, withhold, intract, franchis, long-delay, output, outliv, incurs 
    ##  Topic 8: abraham, fahd, somalia’, mediterranean, el-sheikh, taif, sharm, aziz, barcelona, arabian, paz, damascus, moro, besieg, hotb, thi, righteous, martyr, yoke, confisc 
    ##  Topic 9: gentl, smash, unrepres, sordid, eschew, icrc, muscl, templ, valley, spurn, non-nuclear, plain, hijack, anti-ballist, gloom, rebuff, statesmanship, sanctuari, disposit, non-nuclear-weapon 
    ##  Topic 10: “agenda, test-ban, businesslik, human-resourc, cost-effect, arctic, undp, battalion, non-nuclear-weapon, non-nuclear, iaea, -secretary-gener, troop-contribut, forty-seventh, standard-set, copenhagen, unep, weapon-fre, sofia, step--step 
    ##  Topic 11: countries-, pearson, plata, fantast, kissing, adrift, inter-depend, less-develop, simplic, amort, stanislaw, yalta, precaut, riparian, medit, disarray, lopez, countries—, unhappili, jurist 
    ##  Topic 12: gibraltar, ibero-american, spanish, america’, spain, paz, microcredit, portuguese-speak, revolucionaria, bogota, ortega, argentina’, biennium, josé, uruguayan, asymmetri, multilingu, cartagena, marxist, exponenti 
    ##  Topic 13: extrajudici, “respons, monterrey, system-wid, freedom”, protect”, “develop, mello, ping, sergio, katrina, vieira, thabo, monuc, six-parti, beslan, cologn, icc, quartet, anti-corrupt 
    ##  Topic 14: aung, kyi, suu, obscen, sharon, smart, zimbabwean, ireland, timor, irish, licens, oversea, timor-lest, duty-fre, recommit, reded, netanyahu, poll, countermeasur, downturn 
    ##  Topic 15: romania, pristina, bulgaria, bulgarian, romanian, euro-mediterranean, croatia, south-eastern, transatlant, orthodox, hungari, hungarian, tyrol, dayton, essi, serbian, albanian, euro-atlant, albania, osc 
    ##  Topic 16: coun¬tri, southwest, inter¬n, williamsburg, kittani, northsouth, justice-lov, wechmar, vanuatu, grenadin, salim, thirty-sixth, nonalign, secretarygener, countries—, thirty-seventh, indochines, vincent, superpow, von 
    ##  Topic 17: tela, pitiless, norodom, anc, liberalis, sudano-sahelian, gbadolit, sahraoui, sociolog, reykjavik, jeopardis, mobilis, debt-serv, characteris, maghreb, slow-, deforest, french-speak, major-gener, bean 
    ##  Topic 18: isil, bashar, al-assad, europe’, levant, al-qaida, fractur, crimea, shout, tore, borderless, al-qadhafi, behead, mogen, damascus, buddhist, sleep, haram, second-largest, imam 
    ##  
    ##  Covariate Words:
    ##  Group 0: consult, expedit, decemb, signifi, zone, support, facil, due, implement, issu, outstand, similar, along, enshrin, overwhelm, realiz, inculc, provid, person, extend 
    ##  Group 1: centenni, european, autumn, van, maltreat, censorship, harsher, underlin, nutshel, inward, colleagu, unblock, weekend, unsaf, stricter, everyday, liaison, outward, penalti, appal 
    ##  
    ##  Topic-Covariate Interactions:
    ##  Topic 1, Group 0: presidium, ssr, binari, jong, byelorussian, soviet-unit, leninist, leonid, anti-satellit, ussr, mongolian, lenin, ukrainian, soviet-american, romanian, romania, bulgarian, -european, neutron, viet-nam 
    ##  Topic 1, Group 1: semi-manufactur, jona, transatlant, food-stuff, riidig, dar, nagorno-karabakh, csce, land-lock, aberr, debt-serv, egoism, nigerian, free-market, genet, poster, realis, steal, factori, expuls 
    ##  
    ##  Topic 2, Group 0: liberalis, jeopardis, bradi, revitalis, destabilis, forty-third, intermediate-rang, garba, debt-servic, forty-fourth, utilis, slow-, shorter-rang, characteris, singy, florin, tela, nepal, industrialis, est 
    ##  Topic 2, Group 1: czech, poland, renamo, lyon, wto, communism, kong, sell, bank’, triad, polish, hong, privat, czechoslovakia, rejuven, entrepreneurship, countries’, britain, internet, macroeconom 
    ##  
    ##  Topic 3, Group 0: vorster, reconquest, independencia, houari, somoza, yanke, fretilin, paigc, zimbabwean, zionist, bassa, lackey, agostinho, albania, albanian, saigon, imperialist, turnhall, mauber, mpla 
    ##  Topic 3, Group 1: belgium, leonid, rahman, presidium, acp, belgian, kinshasa, aadd, nine, precept, reproach, phnom, brezhnev, oil-export, happili, degener, dispassion, anguish, retir, wanton 
    ##  
    ##  Topic 4, Group 0: iceland, pearson, latvia, finnish, finland, canadian, norwegian, swedish, liechtenstein, aaddl, lithuania, nordic, reykjavik, canada, lester, unionist, wilson, angi, simplic, arctic 
    ##  Topic 4, Group 1: rapid-react, unprofor, cleansing”, “ethnic, forty-eighth, bosnian, unosom, sarajevo, untac, al-bashir, croat, chechnya, standbi, thunder, pernici, indo, serb, boutros-ghali, bosnia, cis 
    ##  
    ##  Topic 5, Group 0: nagorno, deir, azerbaijani, shatila, sabra, azerbaijan’, azerbaijan, nagorno-karabakh, saddam, karabakh, sharon, iranian, nagorni, tripoli, armenia, lebanes, flimsi, zionist, beirut, iraqi 
    ##  Topic 5, Group 1: landslid, quito, balkan, methodolog, hydrocarbon, win-win, ali, plethora, shelf, skew, jihad, uninhabit, anachronist, “bring, sixty-sixth, catalyt, neighbourhood, frent, â€”, nassir 
    ##  
    ##  Topic 6, Group 0: ncds, acidif, unreport, sid, diabet, kitt, coral, ldc, caricom, taiwan’, montserrat, ldcs, aosi, barbado, dominica, rainforest, abdussalam, geotherm, tobago, mogen 
    ##  Topic 6, Group 1: nagorno, kosovo’, crimea, georgian, pakistan’, malta, ukraine’, gay, malian, afghanistan’, latvia, finland, minsk, russia’, nagorno-karabakh, mali, slovenia, georgia, ossetia, iran’ 
    ##  
    ##  Topic 7, Group 0: al-bashir, eritrean, somalia’, ecomog, ethiopia’, igad, leonean, nigerian, gambian, taylor, igadd, mogadishu, sadc, ethiopian, arap, renamo, liberian, mano, thabo, moi 
    ##  Topic 7, Group 1: unionist, ireland, irish, disinherit, northern, etho, sombr, nation-st, test-ban, major-gener, kuala, lumpur, precept, submarin, unifil, republican, purport, wartim, samir, nationalist 
    ##  
    ##  Topic 8, Group 0: egypt’, hebron, yemen’, land--peac, gcc, tunb, abidin, yemen, zine, hamad, sultan, emir, hashemit, kuwait’, yemeni, musa, abu, tunisia, saleh, maghreb 
    ##  Topic 8, Group 1: itali, italian, maltes, aguirr, malta, encycl, retard, seminar, peruvian, helicopt, incis, south-south, frelimo, community—, equilibrium, defenseless, suffrag, degener, illusori, fatherland 
    ##  
    ##  Topic 9, Group 0: taliban, lankan, pakistan’, rahman, tamil, kabul, kashmir, kashmiri, saarc, afghanistan’, jammu, bhutto, pakistan, rajiv, pakistani, india’, jawaharl, simla, islamabad, bandaranaik 
    ##  Topic 9, Group 1: argentin, falkland, britain, chissano, cocain, venezuelan, lenin, unprovok, antarct, meat, colombian, churchil, rhodesia, zimbabwean, salisburi, british, gorbachev, sail, argentina, botswana 
    ##  
    ##  Topic 10, Group 0: ukraine’, cis, belarus, freita, amar, diogo, aral, kyrgyz, kazakhstan, semipalatinsk, turkmenistan, kyrgyzstan, “renew, reform”, tajikistan, caspian, uzbekistan, demin, razali, amara 
    ##  Topic 10, Group 1: netherland, danish, denmark, nordic, macedonian, dutch, surinam, longterm, sect, covert, biko, revitalis, secretarygener, supervisori, chairperson, corner-ston, hugo, till, condon, tree 
    ##  
    ##  Topic 11, Group 0: volta, food-stuff, rancor, leopoldo, undevelop, semi-manufactur, specious, re-sourc, unctadj, disinherit, geolog, santiago, oil-export, gaston, theolog, malik, hie, hambro, uthant, pauper 
    ##  Topic 11, Group 1: franc, music, anti-satellit, arthur, subservi, smash, fauna, pen, french, demis, punit, gallant, thai, ozon, abort, domain, clear-sight, warhead, antarctica, nurs 
    ##  
    ##  Topic 12, Group 0: peruvian, isthmus, argentin, venezuelan, andean, inter-ocean, paraguay, colombian, montevideo, costa, rica, domingo, guatemalan, paraguayan, quito, salvadoran, coca, rafael, bolivian, tegucigalpa 
    ##  Topic 12, Group 1: portugues, unita, belgium, specious, ghali, timores, didier, portug, lisbon, timor, timor-lest, angolan, maghreb, “agenda, guinea-bissau, chissano, bicess, mozambican, belgian, congoles 
    ##  
    ##  Topic 13, Group 0: sahelo-saharan, ex-combat, ticad, microcredit, francophoni, ezulwini, means”, theo-ben, sixty-sixth, kathmandu, stakehold, burundian, reappoint, nepales, mdgs, deiss, “bring, almati, al-nass, sixty-seventh 
    ##  Topic 13, Group 1: slovakia, austria, slovak, tanzanian, curriculum, islamabad, ctbt, austrian, taliban, seminar, soft, luxembourg, lebanon’, swedish, opium, ahtisaari, post-kyoto, juvenil, npt, ecomog 
    ##  
    ##  Topic 14, Group 0: mururoa, tokelau, fijian, fiji’, niue, polynesia, distant-wat, melanesian, swazi, matignon, tuna, australia’, kanak, atol, fiji, australian, low-li, bougainvill, swaziland, malawi 
    ##  Topic 14, Group 1: lankan, unionist, decommiss, blair, mitchel, tamil, pernici, gay, cluster, buddhist, union-unit, mouth, somalia’, wretch, munit, weep, republican, seattl, agenda”, darfur 
    ##  
    ##  Topic 15, Group 0: macedonian, kosovo’, forty-eighth, samir, csce, malta, croat, unprofor, untac, czech, nagorno-karabakh, boutros-ghali, maltes, cleansing”, yeltsin, “ethnic, gay, eurasia, andorra, austria 
    ##  Topic 15, Group 1: hebron, sacrosanct, francophoni, bangui, abdussalam, â€”, lebanon’, bongo, sheikha, eurasian, al-khalifa, -inclus, ukraine’, cordovez, truce, haya, redeploy, video, landmin, nagorni 
    ##  
    ##  Topic 16, Group 0: phnom, penh, thai, hanoi, vientian, nol, indo, riidig, thailand, lao, minh, samdech, khmer, chi, roug, buddhist, indo-chines, eight-point, lon, laotian 
    ##  Topic 16, Group 1: shatila, sabra, flimsi, disband, non-whit, anti-satellit, rancor, lome, security-build, -stand, polish, covert, thorn, long-rang, dismal, lesotho, ten, sahelian, xxx, non-oil-produc 
    ##  
    ##  Topic 17, Group 0: kinshasa, bangui, bongo, kivu, eyadema, hadj, ndjamena, biya, idriss, togoles, anjouan, mbasogo, senegales, nguema, niger, sassou, nguesso, burkina, togo, abdou 
    ##  Topic 17, Group 1: bradi, twelv, utilis, est, debt-servic, roh, mururoa, destabilis, roug, sadcc, punta, del, pedro, mecca, shorter-rang, sharpevill, isthmus, states-soviet, gorbachev, csce 
    ##  
    ##  Topic 18, Group 0: bibl, georgian, andorra, abraham, america’, music, jesus, shakespear, bag, consumer, theolog, hebrew, song, thunder, castro, chávez, rogu, post-soviet, allah, lula 
    ##  Topic 18, Group 1: diabet, deir, kingdom’, egypt’, geolog, burundian, afghanistan’, belarus, public-priv, minsk, abdullah, umbrella, paus, taliban, france’, protect”, faso, burkina, tribe, yemen 
    ## 

``` r
plot(t20_k24_cont_EU, type = "perspectives", topics = 1)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k24_cont_EU-1.png)

``` r
plot(t20_k24_cont_EU, type = "perspectives", topics = 2)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k24_cont_EU-2.png)

``` r
plot(t20_k24_cont_EU, type = "perspectives", topics = 3)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k24_cont_EU-3.png)

``` r
plot(t20_k24_cont_EU, type = "perspectives", topics = 4)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k24_cont_EU-4.png)

``` r
plot(t20_k24_cont_EU, type = "perspectives", topics = 5)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k24_cont_EU-5.png)

``` r
plot(t20_k24_cont_EU, type = "perspectives", topics = 6)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k24_cont_EU-6.png)

``` r
plot(t20_k24_cont_EU, type = "perspectives", topics = 7)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k24_cont_EU-7.png)

``` r
plot(t20_k24_cont_EU, type = "perspectives", topics = 8)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k24_cont_EU-8.png)

``` r
plot(t20_k24_cont_EU, type = "perspectives", topics = 9)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k24_cont_EU-9.png)

``` r
plot(t20_k24_cont_EU, type = "perspectives", topics = 10)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k24_cont_EU-10.png)

``` r
plot(t20_k24_cont_EU, type = "perspectives", topics = 11)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k24_cont_EU-11.png)

``` r
plot(t20_k24_cont_EU, type = "perspectives", topics = 12)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k24_cont_EU-12.png)

``` r
plot(t20_k24_cont_EU, type = "perspectives", topics = 13)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k24_cont_EU-13.png)

``` r
plot(t20_k24_cont_EU, type = "perspectives", topics = 14)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k24_cont_EU-14.png)

``` r
plot(t20_k24_cont_EU, type = "perspectives", topics = 15)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k24_cont_EU-15.png)

``` r
plot(t20_k24_cont_EU, type = "perspectives", topics = 16)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k24_cont_EU-16.png)

``` r
plot(t20_k24_cont_EU, type = "perspectives", topics = 17)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k24_cont_EU-17.png)

``` r
plot(t20_k24_cont_EU, type = "perspectives", topics = 18)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k24_cont_EU-18.png)

``` r
plot(t20_k24_cont_EU, type = "perspectives", topics = 19)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k24_cont_EU-19.png)

``` r
plot(t20_k24_cont_EU, type = "perspectives", topics = 20)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k24_cont_EU-20.png)

``` r
plot(t20_k24_cont_EU, type = "perspectives", topics = 21)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k24_cont_EU-21.png)

``` r
plot(t20_k24_cont_EU, type = "perspectives", topics = 22)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k24_cont_EU-22.png)

``` r
plot(t20_k24_cont_EU, type = "perspectives", topics = 23)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k24_cont_EU-23.png)

``` r
plot(t20_k24_cont_EU, type = "perspectives", topics = 24)
```

![](unga_2017_analysis_files/figure-markdown_github/t20_k24_cont_EU-24.png)
