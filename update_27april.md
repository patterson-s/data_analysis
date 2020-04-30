``` r
pacman::p_load(stm,
               dplyr,
               quanteda,
               readr,
               xtable)
```

Load Environment
================

``` r
load("update270420.RDataTmp.RData")
```

Topics: t0\_k12\_cont\_EU
=========================

``` r
t0_k12_cont_EU_topics
```

    ## Topic Words:
    ##  Topic 1: helmut, con¬vinc, erich, german-polish, space-bas, states-, andropov, delor, state--st, pragu, scheel, german, gierek, aild, ti-bal, ail-, return—, kohl, abm, honeck 
    ##  Topic 2: l’aquila, cyberspac, gordon, climate-resili, att, gni, ki-moon’, rights-bas, peacebuild, johnson-sirleaf, driver, nature’, obama’, pittsburgh, cybercrim, low-carbon, panel’, -track, post-kyoto, bounc 
    ##  Topic 3: -armament, desta, aouzou, ahidjo, giscard, hissein, rancor, benit, nixon, gaston, yen, shirley, hamilton, ecu, pro-gramm, knell, senghor, portillo, sedar, ever— 
    ##  Topic 4: al-assad’, shia, stadium, stiglitz, kremlin, “democracy”, jam, rouhani’, behead, asleep, wand, lazi, kalashnikov, eisenhow, malala, mh-, luther, musician, tempest, raft 
    ##  Topic 5: slavonia, milosev, todayâ, olara, cost-cut, otunnu, slovak, slovakia, ifor, unosom, standbi, rapid-react, kfor, secretary-generalâ, srebrenica, sarajevo, ctc, high-readi, sirmium, pornographi 
    ##  Topic 6: ii”, kerri, isi, “geneva, syrian-l, ceuta, mistura, qaeda, jihadist, two-stat, syria’, jeremić, melilla, staffan, nagorno, lebanon’, osama, quartet, lakhdar, unamid 
    ##  Topic 7: monuc, marcoussi, bunia, fnl, kivu, kananaski, mouvement, congoles, libérat, cologn, circumcis, intra-palestinian, inter-congoles, zairian, booby-trap, knell, eufor, monuc’, nyerere’, artemi 
    ##  Topic 8: commit¬, terri¬tori, non-lebanes, jordanian-palestinian, accord¬, hag, con¬sider, —israel, karam, effective¬, understand—, devel¬op, unspectacular, nego¬ti, governments—, rights-, united-n, gaza’, restora¬t, docu¬ 
    ##  Topic 9: nkomati, sadcc, pinié, ifad, imp, tad, pre-implement, exchange-r, tela, contadora, sharpevill, shorter-rang, south-north, intermediate-rang, bophuthatswana, venda, botha, muzorewa, view—, pio 
    ##  Topic 10: ibero-american, minugua, mitch, felip, bahia, guatemalteca, palma, pedro, magna, ecumen, carta, argentinean, cruz, blanco, bogota, josé, ibero-america, willpow, bahía, mercosul 
    ##  Topic 11: relation-ship, famagusta, ecumen, non-arma, -selv, dissuas, pan-american, lausann, turkish-cypriot, cogen, peace-bring, islet, adig, mutandi, mutati, maltes, less-advanc, jon, alrevl, non-remov 
    ##  Topic 12: nuclear-weapon-test, unef, mcnamara, hartl, hope-giv, hae, commit-, schistosomiasi, seyn, howe, mekong, countries—develop, assis¬t, cfcs, liberalis, nonnuclear, aiaddl, wmo, forsworn, capitalis 
    ##  
    ##  Covariate Words:
    ##  Group 0: extort, negat, lofti, surround, washington, wisdom, formul, auspic, generous, rostrum, plan, scheme, sympathi, train, prompt, explos, suppress, implement, bloodi, sir 
    ##  Group 1: cfc, swollen·, economic-reconstruct, “platform”, euunit, julyí, aeschylus, isocr, performance-driven, stoel, fyrom, brdo, ever-recur, pay·, schur, “tolerance”, barri, seventy-f, mich, carrington 
    ##  
    ##  Topic-Covariate Interactions:
    ##  Topic 1, Group 0: presidium, husak, todor, soviet-french, ilyich, zhivkov, songun, shcherbitski, ssr, juch, jaruzelski, wojciech, yuri, anti-hitl, korea-unit, ceausescu, binari, anti-soviet, military-strateg, jong 
    ##  Topic 1, Group 1: west-east, german-soviet, poster, recycl, semi-manufactur, biospher, riidig, agit, alonb, contribu, econ, followinghi, forcework, germangerman, omi, sembl, sup, wek, charleston, countries-raw 
    ##  
    ##  Topic 2, Group 0: tongan, tuvalu’, tonga’, unreport, ncds, pan-caribbean, bleach, msg, sid, hfcs, bangla, majuro, lucia’, tobago’, ncd, grenada’, ramsi, nauru’, acidif, redd 
    ##  Topic 2, Group 1: cyberattack, estonia’, hudson, latvia’, slovakia’, estonian, malta, vilnius, latvia, lithuania’, donorship, maltaâ€™, â€œour, â€œrespons, generationsâ€, protectâ€, e-readi, economist”, finno, finno-ugr 
    ##  
    ##  Topic 3, Group 0: europa, siemreap, boke, prat, hoxha, enver, kompong, social-imperi, imperialist-zionist, ngouabi, kerekou, social-imperialist, marien, menelik, azanian, glorieus, dahomey, sekou, reconqu, nol 
    ##  Topic 3, Group 1: aaddl, kite, patience-admir, roza, settled-far, sir-presid, actively—togeth, changes—need, depends—poverti, including—, jobs—, legitimate—, problems—poverti, trialogu, twelve—, yesterday—profound, -frenchmen, case-toward, comes-, franco-soviet 
    ##  
    ##  Topic 4, Group 0: belmar, morazán, disempow, monoth, neo-liber, andorran, lavala, decertifi, andorra’, kirchner, isaiah, psychic, evo, theolog, buddhism, bibl, amia, shakespear, colombia’, consumer 
    ##  Topic 4, Group 1: daesh, cfe, deir, tadeusz, nafusa, zawiyah, againlf, countrywomen, daraa, happen”, islamist-l, kleptocraci, neo-conserv, open-market-bas, theos, al-sheitaat, campuses”, enemies’, ez-zor, isil” 
    ##  
    ##  Topic 5, Group 0: transnistrian, prevlaka, danubian, kuchma, moldovan, niyazov, transdniestrian, guuam, transdniest, nazarbaev, nursultan, moldova’, turkmenistan’, dniester, post-confront, nagorny-karabakh, serbia’, post-communist, abkhazian, cica 
    ##  Topic 5, Group 1: austria’, unamir, minurca, uncitr, wassenaar, near-standstil, e-ecn, kosovska, pluri, syrianlebanes, oneâ, “burden, madariaga, rehn, sharing”, vienna’, â€œto, denmarkâ, indiaâ, smallâ€ 
    ##  
    ##  Topic 6, Group 0: egypt’, mohamud, hadi, abidin, unme, kordofan, sudan’, sana’, yemen’, takfiri, badm, eritrea-ethiopia, hanish, herat, al-shifa, icu, tumb, tfg, unmiss, ethiopia’ 
    ##  Topic 6, Group 1: crimea, bulgaria, séléka, bulgaria’, pristina, latvian, hungari, bokova’, sarafovo, triple-win, unicef-sponsor, child-protect, cyril, disability-inclus, moravia, planet-sensit, rights-driven, methodius, al-husein, youth-specif 
    ##  
    ##  Topic 7, Group 0: mali’, unamir, malian, minurca, alioun, séléka, tutsi, unita’, jona, mano, gnassingbé, debi, oumar, ituri, débi, idriss, ulimo, ange-félix, djohar, lissouba 
    ##  Topic 7, Group 1: merchandis, calculation”, crate, haesendonck, razili, weu’, infected”, -pronounc, often-understand, shake-, verhofstadt, niass, lièg, outgam, broeck, ife-, win-win-win, sub-munit, “travel, “slow-mot 
    ##  
    ##  Topic 8, Group 0: deir, hormuz, shatt-al-arab, basrah, judaea, fahmi, dayan, al-nakba, dimona, samaria, irgun, non-arab, judea, partitionist, al-khalil, euphrat, fahd, imperial-mind, khomeini, balfour 
    ##  Topic 8, Group 1: taoiseach, anglo-irish, belfast, ireland, unionist, irish, europa, obscen, republican, piecem, -certain, aspiration-, based—, changes-except, cyprus—though, detail—, essential-rol, imposed-, inferior—, problems—bas 
    ##  
    ##  Topic 9, Group 0: jayewarden, administrator-gener, ershad, basotho, kairaba, pac, koevoet, premadasa, birendra, chad-libya, siaka, traor, africanist, kolingba, jawara, unban, reed, turnhall, cilss, disinvest 
    ##  Topic 9, Group 1: roh, twelv, hong, arab-israel, kong, churchil, apvpp-, cpc, frontiers·, hein, piet, plaid, single·, your, hard-tri, -exit, countriesdenmark, cunt, heiabe, signn 
    ##  
    ##  Topic 10, Group 0: duart, zuazo, estenssoro, peruvian, fujimori, ecuador’, drug-produc, chamorro, uruguayan, riobamba, bolivia’, panamian, balagu, coca, cerezo, inter-ocean, ricardo, guadalajara, sánchez, amazonian 
    ##  Topic 10, Group 1: spaniard, monua, cplp, romania’, unavem, gibraltar, alioun, timores, xanana, romania, unita’, unita, development-aid, membersw, ever--open, macau’, “ocean, dhlkama, long-protract, gusmao 
    ##  
    ##  Topic 11, Group 0: peron, trawler, enosi, belaund, con-front, geostationari, aaddl, guzman, kreiski, re-sourc, uthant, unctadj, echeverria, spaniard, figueiredo, campin, xxvj, states-, gibraltar, suarez 
    ##  Topic 11, Group 1: greece’, turkey’, ronald, settler, â€œrightâ€, non-norm, organizationâ€™, otherâ€™, turkeyâ€™, vis-ã, waste-wat, cypriot-l, non-cypriot-inspir, karpass, andconvent, crimeóth, goali, missionónam, nego-ti, per-form 
    ##  
    ##  Topic 12, Group 0: roh, re-inscript, johnston, re-inscrib, ecaf, polynesian, maori, evatt, drift-net, singy, arf, matignon, kanak, akayev, jigm, wangchuck, tae, driftnet, mindanao, nam’ 
    ##  Topic 12, Group 1: antill, mors, assume-, banjak, convention-albeit, government-lik, jia, key-word, nations-tens, objective-, others-observ, pjvate, rezeki, rosier, servant-said, thant-, time-much, tve, vocation-, allana 
    ## 

Topics: t0\_k18\_cont\_EU
=========================

``` r
t0_k18_cont_EU_topics
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

Topics: t0\_k24\_cont\_EU
=========================

``` r
t0_k24_cont_EU_topics
```

    ## Topic Words:
    ##  Topic 1: honeck, chemical-weapon-fre, security-build, medium-rang, created—, litigi, reduction—, reykjavik, anti-ballist, govern¬, peace—, mr·, ss-, intermediate-rang, pro¬pos, mikhail, peace¬, general-secretari, missil, con¬vinc 
    ##  Topic 2: rights-bas, gni, att, climate-resili, sector-l, co-host, nations-african, low-carbon, westgat, zero-toler, aftershock, peacebuild, -track, treki’, country-specif, busan, driver, gordon, “geneva, florida 
    ##  Topic 3: persh, hai, interparliamentari, people—, fantast, least-advanc, ripost, slander, inde¬pend, warlik, wild, govern¬, high-handed, falsehood, debt—, good-neighborli, diem, nonalign, gaull, smile 
    ##  Topic 4: crimea, sicken, cyberattack, tallinn, crimean, lagrant, holodomor, tatar, estonia, gay, minsk, isil, mh-, “geneva, cyber, poland’, onlin, yazidi, internet, synagogu 
    ##  Topic 5: todayâ, olara, otunnu, latvia, intersector, latvia’, rapid-react, pornographi, “cultur, men”, turner, helmets”, â€”, “freedom, landmin, conflict-prevent, brahimi, anti-personnel, iptf, academia 
    ##  Topic 6: ceuta, melilla, ross, khalifa, lebanon’, lakhdar, mohamud, abdullah, “geneva, envoy’, moratino, abdulaziz, rouhani, ould, hebron, hassan, vuk, jeremić, spain’, counterterror 
    ##  Topic 7: monuc, casam, marcoussi, bunia, kivu, mouvement, libérat, national, fnl, unami, conakri, francophon, booby-trap, monuc’, artemi, prophylact, respres, unitaid, monterrey, kinshasa 
    ##  Topic 8: lebanon—, peace¬keep, terri¬tori, con¬tinu, con¬cern, interna¬t, habib, develop¬, recog¬n, inter¬n, coun¬tri, aziz, ismat, hag, eco¬nom, con¬vent, accord¬, fez, con¬sider, gunmen 
    ##  Topic 9: biko, mors, pinié, pre-implement, tad, sadcc, punta, transkei, anglo, southwest, flimsi, dialog, non-whit, thai-kampuchean, population—, est, kyprianou, nkomati, bishop, bast 
    ##  Topic 10: unavem, sfor, guatemalteca, weu, acordo, “agenda, southeastern, seci, bahía, croatian-muslim, portugal’, royaumont, urng, alba, canton, democracies”, humanitarian-aid, cyrus, andorra, ghali 
    ##  Topic 11: famagusta, cyprus’, turkey’, turkish-cypriot, ankara, bizon, greek, papandreou, greec, bi-zon, bi-commun, cypriot, turkish-greek, bicommun, arabisra, turkish, hellen, aegean, turkey, greek-turkish 
    ##  Topic 12: asean’, untac, indo, holbrook, conflict-prevent, peace-keep, link-, unosom, centre-piec, krajina, capitalis, aga, shiit, databas, --frequent, big-pow, post-cold-war, uner, zero-yield, sadruddin 
    ##  Topic 13: al-assad’, hussein’, islamist, post-taliban, isil, clone, authorities’, al-assad, film, anthrax, aylan, malala, third-largest, lict, rabbani, treatabl, gay, imam, inspector, daesh 
    ##  Topic 14: gabriel, argentinean, compliant, argentina’, self-apprais, marxist, bogota, marti, gonzalez, communitarian, kilogram, liberum, anti-histor, asymmetri, farabundo, materialist, felip, jaim, coffe, arra 
    ##  Topic 15: valeri, debut, apprentic, sorcer, desta, quid, giscard, trembl, issa, -armament, european-arab, incorrig, gowon, fortiori, hamilton, africa-, gaston, ahidjo, benit, shirley 
    ##  Topic 16: chiluba, israelí, narrat, post-independ, re-engag, life-sav, baidoa, zimbabwean, unioní, childbirth, mahiga, united-n, janjawe, unrepres, callous, afterthought, blair, union-unit, power-shar, misunderstood 
    ##  Topic 17: slovakia, romania’, slovakia’, slovak, transdniestria, thousandth, transregion, bratislava, khatami, ctc, karzai, inter-ethn, gerd, century”, quartet, post-kyoto, sheikha, opium, beslan, al-khalifa 
    ##  Topic 18: habibi, human-induc, value”, “walk, high-valu, cabl, outcome-ori, duty-fre, downtown, “climat, tsunami, dili, “equal, malta’, mainland, costliest, seeker, largest-ev, friendliest, obscen 
    ##  Topic 19: german-soviet, security-, aaddl, ritualist, countries-, munich, semi-manufactur, malthusian, non-arma, portillo, nations-, lopez, world¬wid, inland, coun, states-regardless, council-canada, aild, declaration-, hair-split 
    ##  Topic 20: stiglitz, rouhani’, throb, manhattan, smash, eisenhow, gentl, peddl, “never, shred, teenag, don’t, mediocr, lincoln, metropoli, drawbridg, corps, roam, unmoor, al-baghdadi 
    ##  Topic 21: esquipula, barco, polaris, bettino, perestroika, roh, nest, materialis, debt-servic, complementarili, untag, craxi, stabilis, hon-align, tela, bradi, symbolis, liberalis, jeopardis, hunan 
    ##  Topic 22: lehman, months’, trade-distort, davo, hedg, public-priv, computer, financial-market, depositor, homeown, globalization’, milk, oxygen, anthropologist, phone, internet, pharmaceut, ruggiero, tariff-fre, pittsburgh 
    ##  Topic 23: ancillari, edvard, aadd, plug, vent, dumbarton, oak, mock, unobtain, leaders-, fellow-memb, glossari, maldistribut, misunderstood, commentari, aiaddl, said-, uncoordin, painless, anglo-french 
    ##  Topic 24: gase, kyoto, emiss, greenhous, germany’, tsunami, temperatur, ozon, transboundari, ever-evolv, clean, unep, layer, montreal, climat, mitig, protocol, rain, forest, manmad 
    ##  
    ##  Covariate Words:
    ##  Group 0: along, robert, constitut, locat, premis, immemori, current, extol, number, consequ, plan, condit, ostens, caus, demonstr, difficult, line, provid, contain, addit 
    ##  Group 1: tehran’, courtroom, idea-forc, risorgimento, territory--peac, abbas’, favourable·, íus, un-thought, -welcom, cjnfine, flemish, yperit, country-ori, kozulin, elbaradei’, myanmarburma, swollen·, “unpredict, ”superhuman 
    ##  
    ##  Topic-Covariate Interactions:
    ##  Topic 1, Group 0: czechoslovak, erich, presidium, andropov, todor, husak, shcherbitski, zhivkov, wojciech, jaruzelski, ceaugescu, ssr, khural, soviet-french, ilyich, songun, anti-hitl, sober-mind, yuri, binari 
    ##  Topic 1, Group 1: justly—, readi¬, colleagues—, denmark—, fragile—econom, sus-pend, rabble-rous, —like, organ¬, unmi, nuclear-fuel, employment-gener, ten, brunei, darussalam, verifi, lowest, cambodian, debt, indebted 
    ##  
    ##  Topic 2, Group 0: ldcs, barbuda, tobago’, pan-caribbean, tuvalu’, dominica’, lucia’, grenada’, oec, bangla, jamaica’, redd, eswatini, banana-produc, kitt, windward, zambia’, barbadian, non-communic, tobago 
    ##  Topic 2, Group 1: arctic, final-status, olmert, bahraini, kosovo’, unrwa, pakistan’, country-own, still-great, rights’, tax-revenu, near-glob, adulteri, “point-seven”, footbridg, marriott, market-sound, israel-syria, multi-trillion-dollar, turkana 
    ##  
    ##  Topic 3, Group 0: europa, heng, samrin, penh, social-imperi, siemreap, prat, tonl, walker, battambang, second-world, quintal, anti-chines, social-imperialist, hoxha, enver, phnom, hua, corinto, kam¬puchea 
    ##  Topic 3, Group 1: blum, caledonian, mururoa, anti-satellit, another—econom, belong—mad, briand, cleverest, edgard, enough—although, familiar—, herriot, idea—, longer—, oroken, overwarm, progress—difficult, supported—, terms—assum, tests—controversi 
    ##  
    ##  Topic 4, Group 0: georgia’, non-albanian, chechen, kosovo’, serbia’, ossetian, sukhumi, tskhinvali, armenian-azerbaijani, metohija, eulex, tbilisi, abkhazian, azerbaijan’, armenia’, moldovan, kyiv, abkhaz, baku, azerbaijani 
    ##  Topic 4, Group 1: isi, cybercrim, staffan, feather, valletta, smell, defil, daesh, behead, narrat, -years’, cyberspac, lemkin, raphael, digit, tempest, “fulli, co-ethn, lefortovo, long-discredit 
    ##  
    ##  Topic 5, Group 0: marino, monaco, princess, chile’, war-affect, canada’, winnipeg, canadian, dividend”, “renew, cedaw, liechtenstein, organizationâ, malta’, reform”, rapid-deploy, prehistor, peopleâ, oil--food, clone 
    ##  Topic 5, Group 1: austria’, austria, kfor, herzegovina’, chechen, non-albanian, austrian, stomach, tyrolean, tashkent, undcp, milosev, salman, oneâ, â€œto, denmarkâ, indiaâ, smallâ€, antidote”, cities” 
    ##  
    ##  Topic 6, Group 0: bahraini, egypt’, salman, abdrabuh, benomar, al-nahyan, emirati, emirates’, al-jab, alija, al-shura, al-saud, derna, oman’, hadi, abidin, unrwa’, gcc, tumb, food” 
    ##  Topic 6, Group 1: spaniard, gibraltar, spain, ibero-american, reincorpor, palma, spanish, séléka, ibero, stage”, biomedicin, oviedo, cádiz, full-throat, iaea’, spain-unit, valencia, murcia, “failures”, sahraqui 
    ##  
    ##  Topic 7, Group 0: burundi’, minurca, mali’, tutsi, houphouët-boigni, alioun, mano, séléka, ramos-horta, bangui, idriss, abdoulay, gabon’, cplp, copax, compaoré, togo’, défens, itno, ondimba 
    ##  Topic 7, Group 1: unta, anarchist, merchandis, ami, abyei, -pronounc, often-understand, shake-, calculation”, crate, haesendonck, razili, weu’, infected”, niass, “slow-mot, luvungi, three-step, lièg, outgam 
    ##  
    ##  Topic 8, Group 0: deir, hormuz, jewri, bani-sadr, khanaqin, barzani, al-nakba, shatt-al-arab, haaretz, mosh, qibya, weizmann, defac, qasim, kafr, lavon, fahmi, basrah, judaea, dayan 
    ##  Topic 8, Group 1: demarch, restaur, -promis, arisen-sever, assassinated-, outside-, supported-, borrow—, just—world, long-canvass, malthus, prosperity—wil, andconvent, crimeóth, goali, missionónam, nego-ti, per-form, remainóa, remainsóshould 
    ##  
    ##  Topic 9, Group 0: sensitis, turnhall, birendra, reed, xix, jomo, ever-escal, langa, supremacist, bantu, countervail, imr, bigpow, mzee, siaka, choudhuri, sobhuza, humayun, illueca, jawaharl 
    ##  Topic 9, Group 1: israel-arab, mekong, danish, countries-concern, recycling—, developing—publ, djibouti—, vulnerability—, countriesdenmark, cunt, heiabe, signn, tual, —firm, effect-, europe-whos, fruitful-wil, -exit, -intern, cept 
    ##  
    ##  Topic 10, Group 0: croatia, herzegovina’, icti, bulgaria’, unta, croat, croatia’, herzegovina, unprofor, croatian, forty-eighth, danubian, unmop, kosova, albania’, macedonia, bosnia, serb, slovenia, serbian 
    ##  Topic 10, Group 1: xanana, cplp, ramos-horta, alioun, macao, portuguese-speak, bicess, portugues, timores, lisbon, unita, issa, missionari, ibero-american, terrestri, santa, unidad, ibero, unita’, angolan 
    ##  
    ##  Topic 11, Group 0: tyrol, tyrolean, german-speak, valletta, partitionist, enosi, rauf, greek-cypriot, austrian, malta, ataturk, kreiski, kemal, austria, euro-mediterranean, gibraltar, ever-escal, craxi, americansoviet, inter-commun 
    ##  Topic 11, Group 1: island’, greece’, acqui, pan-american, fahd, small-island, cypriot-l, karpass, fenced-, møller, cypriot-own, non-cypriot-inspir, “fact”, ciller, gávdhos, greek-bulgarian, ioannina, nesto, varna, â€œrightâ€ 
    ##  
    ##  Topic 12, Group 0: myanmar, arf, nam’, ecaf, cambodia’, mindanao, nepales, wangchuck, singy, jigm, burma, nepal, yen, thai, thailand’, asean, kathmandu, mekong, dev, bikram 
    ##  Topic 12, Group 1: sahnoun, kinkel, unprofor, zepa, greenland, cyrus, bosnian, unamir, croat, peace-enforc, houphouët-boigni, forty-eighth, cleansing”, “ethnic, hebron, german-speak, italy’, goma, hutu, oscar 
    ##  
    ##  Topic 13, Group 0: pakistan’, isi, tamil, lankan, shahe, taliban’, mohtarma, herat, ltte, eelam, lanka’, benazir, kandahar, begum, rakhin, kashmiri, mujibur, premadasa, acd, jirgah 
    ##  Topic 13, Group 1: foregon, greek-cypriot, non-communic, -fli, deir, libya’, diabet, fatf, al-qadhafi, nafusa, zawiyah, al-sheitaat, campuses”, enemies’, ez-zor, isil”, klansmen, quasi-mediaev, againlf, countrywomen 
    ##  
    ##  Topic 14, Group 0: argentin, latin-american, duart, ibero-american, uruguayan, quito, isthmus, paz, venezuelan, unidad, cordova, cordillera, hay-bunau-varilla, belic, condor, zuazo, torrijoscart, balboa, vinicio, quetzal 
    ##  Topic 14, Group 1: hungari, sensitis, marginalis, broeck, ife-, aqain, forc«, mimesi, cowri, migliuolo, needier, us-ussr, “hungari, communist-socialist, dumping”, itr, nex, non-pot, wastewat, andeconom 
    ##  
    ##  Topic 15, Group 0: sese, bourguiba, seko, dahomey, ngouabi, kountch, seyni, marien, ifni, bokassa, volta, gnassingb, ndjamena, paigc, oro, caetano, jean-claud, -equip, partido, africano 
    ##  Topic 15, Group 1: guide-lin, pro-gramm, elia, swirl, menachem, latin-american, guineabissau, aadd, inter-depend, kite, patience-admir, roza, settled-far, sir-presid, beew, pie-judg, states-keep, stillwithin, successful-, -contrari 
    ##  
    ##  Topic 16, Group 0: al-bashir, eritrean, abyei, unamid, amisom, sudan, kordofan, unme, icu, eritrea-ethiopia, tfg, ethiopia’, eritrea’, badm, unmiss, nif, mele, kiir, omer, menelik 
    ##  Topic 16, Group 1: anglo-irish, ireland, unionist, irish, sharon, europa, robben, belfast, decommiss, templat, non-lebanes, ground-rul, takes-, resulted”, afrca, hillsborough, hiyher, often-declar, pinii, aiken’ 
    ##  
    ##  Topic 17, Group 0: tashkent, uzbekistan, tajikistan, belarus, kazakhstan’, kyrgyz, darya, nazarbaev, cica, akayev, ashgabat, emomali, aral, tajikistan’, karimov, nursultan, niyazov, bishkek, kyrgyzstan’, lukashenka 
    ##  Topic 17, Group 1: bulgaria’, ecumen, romania, greener, icti, minurca, pristina, bulgaria, attorney, bulgarian, kosovar, unamid, authorities’, croatia’, romanian, “gas, bulgariaundp, seacaspian, areas’, fredrik 
    ##  
    ##  Topic 18, Group 0: xanana, caledonian, australian, bougainvillean, bougainvillian, border-cross, polynesian, polynesia, nasonini, laisenia, qaras, rotuman, lagoon, msg, distant-water-fish, “yokwe”, pccp, caledonia’, nerrdp, nadi 
    ##  Topic 18, Group 1: malta, ntc, maltes, quota-fre, euro-mediterranean, “nurs, diptych, jibreel, mediterranean”, ntc’s, commission-leagu, marco’, “downsizing”, “shadow”, “wins”, ajip, civil-society-bas, lokichokio, mallon, mcalees 
    ##  
    ##  Topic 19, Group 0: pro-gramm, unctadj, short-com, african-asian, guineabissau, guide-lin, s-vii, spaniard, gaston, hamilton, aadd, leopoldo, aladdl, hoffman, stanislaw, re-sourc, shirley, amerasingh, subsoil, addl 
    ##  Topic 19, Group 1: west-east, franco-german, helmut, kohl, erich, co¬oper, gene, andropov, locomot, european-arab, cmea, persh, -set, enemy-imag, extinction·, far-read, force©, indateriali, survival·, value-system 
    ##  
    ##  Topic 20, Group 0: restaur, smell, unidentifi, belmar, monoth, morazán, libel, shanty-town, messiah, ufo, saviour, isaiah, “death, evo, shakespear, marx, einstein, jewel, slumber, movi 
    ##  Topic 20, Group 1: cfe, arab-israel, falkland, hong, dermatolog, fifth-centuri, flavius, flood’, hodel, lapland, pradesh, publius, reagan’, renatus’, sunglass, uttar, vegetius, wide-brim, will￼unfortun, alsace-lorrain 
    ##  
    ##  Topic 21, Group 0: renamo, marginalis, ecomog, unmil, bicess, npfl, pattaya, akosombo, ulimo, indlovukazi, dlvoir, unomil, unban, inkatha, boipatong, swazi, malawian, bakili, muluzi, mswati 
    ##  Topic 21, Group 1: pedro, jewri, cmea, lubber, ruud, pay·, schur, aristegui, contus, oon, precursor-produc, cfc, effort·, much-rep, seal·, standardis, stast, adriessen, blu, un-ment 
    ##  
    ##  Topic 22, Group 0: brazil’, bolaño, yasuní, garcía, cicig, bolivia’, paraguay’, colombia’, leonel, coca, paraguayan, ecuador’, unasur, itaipu, yacyreta, cardoso, peru’, instraw, sánchez, celac 
    ##  Topic 22, Group 1: poland’, l’aquila, britain’, italy’, effort”, geography”, védrine, agriculture’, finno-ugr, e-readi, economist”, finno, information-poor, information-rich, ugric, briceño, levi-montalcini, valero, “lead, canut 
    ##  
    ##  Topic 23, Group 0: brooksrandolph, psychic, angi, randolph, unmind, bahamian, halfheart, vietcong, gavel, pearson, decri, trim, jar, guyana’, micro-st, defil, addl, aaddl, uthant, approb 
    ##  Topic 23, Group 1: precinct, britain’, eclac, “reaffirming”, “recovering”, “renovation”, bang”, invented”, surgeon”, troop-suppli, footpath, outrank, “northern”, lipservic, rights-viol, “constant, shopping-mal, standby-arrang, “cross-cutting”, “ground 
    ##  
    ##  Topic 24, Group 0: arctic, iceland, trawl, kathi, seamount, eez, remengesau, near-shor, oceanscap, palau’, ocean’, bowl, shark, terrestri, sosa, palauan, micronesia, kom, sdg, majuro 
    ##  Topic 24, Group 1: suppli, safeti, energi, ki-moon, panel, research, tsunami, chang, kyoto, forest, emiss, gase 
    ## 

Topics: t10\_k12\_cont\_EU
==========================

``` r
t10_k12_cont_EU_topics
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

Topics: t10\_k18\_cont\_EU
==========================

``` r
t10_k18_cont_EU_topics
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

Topics: t10\_k24\_cont\_EU
==========================

``` r
t10_k24_cont_EU_topics
```

    ## Topic Words:
    ##  Topic 1: tadeusz, edward, hot-b, postwar, root-caus, vietnam, poland, nicaraguan, speediest, viet-nam, indo-chines, polish, vientian, allend, communism, xxii, falkland, subcontin, pre-war, vladivostok 
    ##  Topic 2: rights-bas, one”, climate-resili, “geneva, women’, low-carbon, law”, obama’, country-specif, michell, panel’, state-build, busan, monk, seafar, gender, ii”, quartet’, munit, peacebuild 
    ##  Topic 3: kissing, roger, dishonor, yen, smash, salisburi, nixon, benit, iberian, rancor, dupe, lust, feign, world-, beforehand, organization-, mojsov, falsehood, makario, muzorewa 
    ##  Topic 4: unosom, latvia’, cost-cut, latvia, turner, unprofor, ground-break, cleansing”, standbi, rapid-react, well-train, “ethnic, bosnian, ayala, chechnya, anti-personnel, helmets”, unpaid, clearanc, yitzhak 
    ##  Topic 5: magistr, inter-african, congoles, leopold, kinshasa, zairian, codesa, egoism, inter-congoles, kivu, fortiori, congo, mouvement, institution’, zair, sociolog, belgian, demon, pillag, mobutu 
    ##  Topic 6: lindh, anna, todayí, beslan, terrorists’, qaeda, vieira, sergio, mello, osama, anthrax, conflict”, annan’, hindu, clone, seattl, mitchel, iraq’, countryí, monterrey 
    ##  Topic 7: arab-israel, kurd, ottoman, disfigur, aziz, gangster, saddam, jewri, taif, pere, barb, ida, iraq-iran, oil-produc, norwegian, hijack, phantom, iraqi, athen, kidnapp 
    ##  Topic 8: semi-manufactur, good-neighbor, states-, salaam, bristl, food-stuff, oil-produc, co-op, focal-point, world-, citadel, opec, bicommun, non-european, world-wid, xxi, endeavor, -exploit, indochina, colombo 
    ##  Topic 9: ifad, maladjust, exchange-r, debt-servic, -exploit, etho, slow-, globalis, asymmetri, refinanc, amort, textil, cereal, com, reschedul, insul, concession, debt-serv, non-inflationari, subtl 
    ##  Topic 10: aadd, mcnamara, one-, rod, beforehand, kissing, xxvii, vent, nonintervent, xxiii, modicum, longterm, xxii, addl, rhodesia, short-com, monsoon, postwar, salisburi, connexion 
    ##  Topic 11: â€”, uruguayan, grower, delegitim, pornographi, anti-poverti, gurirab, justice”, louis, governments’, lula, anti-democrat, trivial, prostitut, invis, fifty-third, multicultur, theo-ben, consensus-bas, clone 
    ##  Topic 12: “climat, obscen, typhoon, condominium, sharon, major-gener, decommiss, unchart, sat, unifil, metr, ireland’, england, ozon, test-ban, clinton, troop-contribut, deton, reimburs, submarin 
    ##  Topic 13: ould, issa, kerri, spain’, tunisian, riyadh, khalifa, maghreb, sheikh, nassir, houston, lakhdar, vuk, jeremić, abdulaziz, ghali, rouhani, continent’, kfor, intercultur 
    ##  Topic 14: magistr, reykjavik, williamsburg, anti-satellit, cfe, country—, superpow, nuclear-arm, indira, flash-point, smile, condominium, warhead, weapons—, denuclear, ural, notif, intermedi, ballist, cruis 
    ##  Topic 15: romania, pristina, bulgaria’, hungari, romanian, bulgaria, transregion, bulgarian, transdniestria, slovenia, orthodox, ossetia, herzegovina’, danub, hungarian, croatia’, interreligi, caspian, bucharest, law” 
    ##  Topic 16: phone, turnov, e-govern, public-priv, gordon, computer, mall, entrepreneur, gdp, internet, gender-bas, bank’, milk, telephon, pension, pharmaceut, hiv, digit, export-ori, gender 
    ##  Topic 17: scotland, garang, ami, fnl, libérat, wye, kivu, monuc, unpaid, ehud, hipc, bamako, quartet’, abyei, conakri, intra-st, chiluba, congo, ramallah, unmik 
    ##  Topic 18: martiniqu, guadeloup, human-induc, immediaci, holist, katrina, psychotrop, nature’, oceanograph, sterl, transatlant, fifty-ninth, debilit, policymak, unborn, monterrey, development”, beach, intraregion, interconnected 
    ##  Topic 19: interna¬t, gemayel, habib, eco¬nom, fahd, con¬cern, situa¬t, pre-implement, states—, southwest, com¬mun, tum, year—, perforc, con¬tinu, charter—, negotia¬t, sedar, williamsburg, coun¬tri 
    ##  Topic 20: slovakia, slovak, high-qual, baranja, servicemen, apec, fine-tun, anti-personnel, forty-seventh, expo, razali, boutros-ghali, anti-crisi, freita, amar, conflict-prevent, vancouv, weapons-grad, boutro, fifty-first 
    ##  Topic 21: cruz, sub-commiss, santa, jaim, marxist, bogota, tela, spaniard, contra, punta, pedro, natter, est, guerrilla, cuellar, democratis, cathol, asymmetri, farabundo, perez 
    ##  Topic 22: al-assad’, mh-, islamist, history’, shia, al-assad, terrorism”, naïv, raft, bashar, second-largest, benghazi, nato’, bourguiba, imam, auschwitz, cult, dodg, bus, justice” 
    ##  Topic 23: bizon, bi-commun, ankara, bi-zon, cypriot, bicommun, turkish, turkish-cypriot, hest, cyprus, ploughshar, major-gener, pre-, flew, greek-cypriot, invas, non-whit, demilitaris, result-ori, denktash 
    ##  Topic 24: mekong, kampuchean, eight-point, midterm, norodom, roug, resettl, sihanouk, kampuchea, indochina, interf, co-chairmen, non-aggress, five-point, monopol, cordial, southeast, princ, hanoi, miracul 
    ##  
    ##  Covariate Words:
    ##  Group 0: line, newli, support, implement, confid, join, extol, gracious, consult, steep, annal, fulli, intern, purview, propon, enter, accord, welfar, provis, sever 
    ##  Group 1: carrington, van, european, olmert, crisis-manag, autumn, allur, ready-mad, initial, weeks’, relativ, weekend, harsher, dossier, milosev, nutshel, inward, underlin, tuesday, enquiri 
    ##  
    ##  Topic-Covariate Interactions:
    ##  Topic 1, Group 0: honeck, persh, erich, andropov, presidium, shcherbitski, jaruzelski, husak, brezhnev, ilyich, todor, zhivkov, ssr, anti-hitl, anti-soviet, revanch, byelorussian, ceausescu, byelorussia, military-strateg 
    ##  Topic 1, Group 1: italian, itali, cross-road, unto, peruvian, focal-point, aloud, seminar, incis, equilibrium, patrimoni, amerasingh, aguirr, czech, thirty-first, suffrag, aegean, havel, waldheim, helicopt 
    ##  
    ##  Topic 2, Group 0: kutesa, emitt, sixty-ninth, abdussalam, boko, haram, ebola, sixty-eighth, tuvalu’, nassir, stage”, ldc, cybercrim, lood, avian, jamaica’, lead-, jeremi, nepal’, brockmann 
    ##  Topic 2, Group 1: bahraini, frías, councilí, finland, pakistan’, guam, kosovo’, afghanistan’, russia’, grandpar, afghani, lithuania, anti-poverti, haiti’, monrovia, sweden, abkhazia, anti-semit, finnish, mbeki 
    ##  
    ##  Topic 3, Group 0: social-imperi, social-imperialist, hoxha, enver, ngouabi, glorieus, cia, marien, reconqu, caetano, amus, mengistu, cliqu, yanke, independent, proletariat, fretilin, nol, lon, bassa 
    ##  Topic 3, Group 1: aaddl, yaound, menachem, s-vl, latin-american, short-com, thant, simplic, leonid, pearson, el-sadat, jar, guide-lin, simla, acp, s-vii, equilibrium, delet, alec, issa 
    ##  
    ##  Topic 4, Group 0: monaco, stoyan, halifax, ganev, canada’, freita, estonia, amar, essi, diogo, estonian, lithuania, ghali, forty-seventh, forty-ninth, boipatong, malta’, liechtenstein, slovak, samir 
    ##  Topic 4, Group 1: unamir, greenland, glass, tyrolean, croat, hutu, tutsi, nagorno-karabakh, burundi’, thunder, tiger, macedonian, serb, missionari, wmds, cis, number-on, killer, dougla, sfor 
    ##  
    ##  Topic 5, Group 0: aouzou, malian, bamako, hissein, bongo, compaoré, kolingba, debi, nguema, idriss, ondimba, obiang, mbasogo, chad-libya, togoles, compaor, ecca, senegales, gabon’, comorian 
    ##  Topic 5, Group 1: spaak, specious, belgium, paul-henri, monuc, amman, merchandis, icrc, side-effect, nehru, slander, belgian, plead, paz, lee, duchi, tanzanian, postur, -site, ministri 
    ##  
    ##  Topic 6, Group 0: isi, pakistan’, al-qaida, daesh, eelam, kashmiri, ltte, lanka’, jammu, tamil, isil, myanmar’, jihad, india’, lanka, tashkent, sri, lankan, poppi, saarc 
    ##  Topic 6, Group 1: thabo, amman, anti-fascist, nepad, georgia’, bougainvill, soft, decade-long, sadist, -fli, belarus, peace-build, post-conflict, cancún, kyoto, sudanes, balkan, darfur, osc, israeli-palestinian 
    ##  
    ##  Topic 7, Group 0: deir, judea, samaria, hafez, khomeini, euphrat, -fli, jar, menachem, scotland, hebron, syria, yassin, residenti, sharon, lebanon’, ramallah, stoog, rejectionist, inter-arab 
    ##  Topic 7, Group 1: full-scop, restaur, utilis, mobilis, falkland, argentin, vancouv, nkomati, cfe, realis, industrialis, hong, institutionalis, destabilis, kong, lenin, renamo, gorbachev, sat, chissano 
    ##  
    ##  Topic 8, Group 0: s-vii, amerasingh, tyrolean, shirley, hamilton, gaston, mojsov, s-vij, con-front, lazar, tyrol, s-vi, makario, short-com, guin, lievano, smith, biko, kissing, connexion 
    ##  Topic 8, Group 1: kohl, gene, helmut, erich, honeck, halifax, andropov, jona, german, salin, schmidt, co-respons, abm, duma, riidig, persh, underemploy, germani, co¬oper, egocentr 
    ##  
    ##  Topic 9, Group 0: post-industri, volta, oil-produc, oil-export, underemploy, symmetr, semi-manufactur, petroleum-produc, perforc, foreign-exchang, remun, food-stuff, cocoa, opec, northsouth, condominium, oil-import, tonn, gnp, longterm 
    ##  Topic 9, Group 1: roh, esquipula, barco, duma, shorter-rang, punta, pio, est, tela, bradi, twelv, florin, gbadolit, onion, untag, forty-third, shevardnadz, marginalis, iraq-iran, forty-second 
    ##  
    ##  Topic 10, Group 0: thant, brooksrandolph, uthant, defoli, randolph, pearc, angi, aaddl, width, east-, specious, unconsci, vietnam, geolog, unmitig, litig, nixon, wide-spread, kai-shek, peace- 
    ##  Topic 10, Group 1: antill, netherland, sub-commiss, s-vii, biko, columbus, al-bashir, plutonium, music, hugo, gilbert, soweto, surinam, seychell, fission, transkei, weapons-grad, reprocess, thirty-first, genscher 
    ##  
    ##  Topic 11, Group 0: mercosur, peru’, colombia’, fujimori, ecuador’, chile’, bolivia’, peruvian, cocain, mexico’, brazil’, narco-terror, unasur, calderón, brazilian, luiz, coca, bric, brasilia, attorney 
    ##  Topic 11, Group 1: pittsburgh, poland’, cesar, neck, ortega, cologn, abm, obama’, jeddah, srgjan, brockmann, l’aquila, zagreb, rebuf, d’escoto, riyadh, georgian, post-crisi, barack, bolivarian 
    ##  
    ##  Topic 12, Group 0: caledonian, iceland’, bougainvill, hebrid, mururoa, australian, honiara, trawl, noumea, tokelau, fijian, majuro, drift-net, marshalles, auckland, iceland, ramsi, polynesia, fiji’, niue 
    ##  Topic 12, Group 1: belfast, unionist, anglo-irish, irish, mitchel, ireland, dublin, disinherit, kuala, lumpur, danub, republican, disfigur, northern, clever, scandal, divin, pervas, paramilitari, agenda” 
    ##  
    ##  Topic 13, Group 0: egypt’, bahraini, abidin, mousa, al-saud, tunb, zine, gcc, hamad, tumb, taya, yemen’, sana’, jordan’, algeria’, arab-islam, morocco’, omani, maaouya, land--peac 
    ##  Topic 13, Group 1: portugal’, cplp, ibero-american, spaniard, non-self, independência, união, pablo, portuguese-speak, gibraltar, timores, unita, reincorpor, mali’, portug, america’, delegitim, portugues, heartbreak, eurasian 
    ##  
    ##  Topic 14, Group 0: full-scop, valletta, malta, maltes, euro-mediterranean, scottish, jawaharl, non-nuclear-weapon, megawatt, test-ban, npt, rajiv, nuclear-weapon, nonnuclear, swedish, fission, arms-control, non-prolifer, rouhani, nuclear-weapon-fre 
    ##  Topic 14, Group 1: caledonian, french-speak, aouzou, mururoa, inde¬pend, persh, indo, unmind, franc, isthmus, honeck, france’, desta, knesset, plata, gaull, kigali, hindu, com-mun, pierr 
    ##  
    ##  Topic 15, Group 0: macedonian, turkey’, vilnius, azerbaijani, croatian, nagorno-karabakh, marino, armenia, unmik, armenian, albania’, moldovan, metohija, azerbaijan’, serbia’, tbilisi, armenia’, post-communist, macedonia, baku 
    ##  Topic 15, Group 1: ecumen, attorney, undcp, forum’, gendarm, high-tech, tashkent, timelin, people-centr, austria, amisom, malian, anti-corrupt, poppi, interfaith, ouagadougou, greener, country-specif, isi, nassir 
    ##  
    ##  Topic 16, Group 0: smallhold, microcredit, bangabandhu, rain-f, -five, malawi’, malawian, ziaur, surinames, gambian, alhaji, maiz, health-car, surinam, cubic, malawi, anti-corrupt, nkurunziza, uganda’, biofuel 
    ##  Topic 16, Group 1: cybercrim, estonian, vilnius, estonia, eurozon, cyber, emitt, hammarskjöld, gleneagl, lithuanian, hong, britain, kong, mew, nagorno, “develop, fifty-eighth, kingdom’, virtuous, un-women 
    ##  
    ##  Topic 17, Group 0: unita’, amisom, al-bashir, thabo, inter-congoles, mali’, eritrean, ethiopia’, kabbah, igad, nepad, tejan, leonean, unamsil, ruf, indlovukazi, tanzania’, liberia’, museveni, taylor 
    ##  Topic 17, Group 1: aung, kyi, suu, six-parti, lebanon’, protect”, gnp, “toward, unrwa, luxembourg, jack, “respons, euro, mindset, jeremić, templat, npt, israeli-lebanes, flotilla, vientian 
    ##  
    ##  Topic 18, Group 0: non-communic, island’, bahamian, oec, lucia’, windward, haiti’, grenada’, barbadian, pan-caribbean, montserrat, kitt, jamaican, banana-produc, tobago, trinidad, jagan, tromelin, ramgoolam, caricom 
    ##  Topic 18, Group 1: malta’, malta, maltes, hotspot, euro-mediterranean, tsunami, “climat, migrant, sheikha, guido, home-grown, rabat, clinic, treki, abdussalam, mediterranean, sixty-fourth, asylum-seek, libyan, decade-long 
    ##  
    ##  Topic 19, Group 0: inde¬pend, ifni, bourguiba, ahgr, tamuz, riidig, rudig, xviii, greatpow, traor, africanist, freetown, xix, jaim, jorg, hamra, judaiz, iraqi-iranian, monrovia, qau 
    ##  Topic 19, Group 1: inter-arab, valeri, hebrid, unmitig, mast, denkta, thai-kampuchean, century-old, gendarm, duart, indochines, presidium, lazar, encycl, justice-lov, biko, intermediate-rang, mayott, lievano, disband 
    ##  
    ##  Topic 20, Group 0: belarus, kyrgyz, ashgabat, nursultan, nazarbaev, bishkek, turkmenistan’, karimov, kuchma, kazakhstan’, tajikistan’, uzbekistan’, aral, cica, caspian, dushanb, semipalatinsk, mongolia’, tajikistan, “water 
    ##  Topic 20, Group 1: italy’, blondin, bey, unita’, bicess, hebron, essi, euro-mediterranean, monaco, amara, andorra, stoyan, alioun, unprofor, bosnian, weu, ganev, nafta, asean’, herzegovina 
    ##  
    ##  Topic 21, Group 0: ibero-american, duart, latin-american, martí, argentin, ecumen, isthmus, quito, costa, inter-ocean, rodrigo, amphictyon, itaipu, balagu, juarez, montevideo, alfredo, sucr, ayacucho, stroessner 
    ##  Topic 21, Group 1: liberalis, terrestri, specialis, portuguese-speak, sese, seko, characteris, sadcc, nkomati, renamo, onion, portug, jeopardis, chissano, timores, untag, recognis, mozambican, cemeteri, undaunt 
    ##  
    ##  Topic 22, Group 0: restaur, saviour, bibl, consumer, neo-liber, vultur, song, shakespear, mose, glass, jewel, lust, evo, neck, isaiah, america’, guantánamo, einstein, theolog, sweet 
    ##  Topic 22, Group 1: daesh, germany’, smallhold, minsk, ebola, valletta, asia-europ, geolog, isi, deir, ukrainian, tornado, mogen, jihad, hitler, egypt’, sixty-ninth, burundian, annan’, gender-bas 
    ##  
    ##  Topic 23, Group 0: sadcc, destabilis, patti, characteris, florin, forty-third, caputo, liberalis, untag, tela, marginalis, forty-second, denkta, realis, guido, nkomati, koevoet, dant, utilis, prise 
    ##  Topic 23, Group 1: acqui, island’, turkey’, greece’, athen, greec, neo-liber, gambari, tirana, papandreou, greek-turkish, landslid, quito, uninhabit, passport, macedonia, hydrocarbon, bucharest, albanian, obfusc 
    ##  
    ##  Topic 24, Group 0: thai-kampuchean, china-africa, thai, nam’, nepal, kuala, lumpur, roh, thailand’, angkor, penh, dev, phnom, kim, thailand, philippin, cambodia’, six-parti, asia-europ, asean 
    ##  Topic 24, Group 1: danish, denmark, botha, nordic, sadcc, anti-satellit, non-whit, nkomati, lesotho, undp, finnish, high-prior, troop-contribut, introductori, self-right, program, boycott, arab-isra, copenhagen, open-minded 
    ## 

Topics: t20\_k12\_cont\_EU
==========================

``` r
t20_k12_cont_EU_topics
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

Topics: t20\_k18\_cont\_EU
==========================

``` r
t20_k18_cont_EU_topics
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

Topics: t20\_k24\_cont\_EU
==========================

``` r
t20_k24_cont_EU_topics
```

    ## Topic Words:
    ##  Topic 1: german, pan-european, seven-point, good-neighbor, states-soviet, monopolist, ural, intermediate-rang, reykjavik, longterm, polish, demilitaris, moscow, nonalign, czechoslovak, hegemon, quadripartit, reagan, renunci, medium-rang 
    ##  Topic 2: export-ori, lyon, concession, hong, oil-import, duty-fre, underemploy, textil, non-oil, napl, kong, wto, macroeconom, fiscal, zero-sum, indonesian, downturn, burmes, debt, aggreg 
    ##  Topic 3: world-, shirley, stupid, lazar, hamilton, biko, pitiless, kissing, amerasingh, gaston, mojsov, thirty-first, transkei, sadat, gallant, short-com, salisburi, rhodesia, thirty-second, oil-produc 
    ##  Topic 4: estonia, estonian, stabilis, micronesia, liberalis, jeopardis, pan-european, destabilis, kuwait, nest, mobilis, utilis, characteris, realis, vladivostok, glasnost, csce, klerk, communism, mikhail 
    ##  Topic 5: nagorno, kurdish, syria, syrian, saddam, ugliest, nagorno-karabakh, isi, jew, levant, islam, shrine, self-rul, mosqu, moussa, tehran, karabakh, another’, inspector, regime’ 
    ##  Topic 6: obama’, cross-cut, arctic, post-, “bring, driver, un-women, mdgs, tsunami, low-carbon, rules-bas, want”, means”, al-nass, gender, kutesa, co-host, gender-bas, women’, home-grown 
    ##  Topic 7: misde, unosom, clan, re-engag, power-shar, devolut, rape, inter-st, republican, mogadishu, peace-build, incurs, maim, charl, appeas, dispatch, extremist, wreak, wanton, counterproduct 
    ##  Topic 8: euro-mediterranean, ould, el-sheikh, sharm, khalifa, maghreb, barcelona, jeremi, paz, jamahiriya, détent, tunisian, concord, cairo, relaunch, israeli-arab, hassan, martyr, mediterranean, opertti 
    ##  Topic 9: gentl, muscl, textil, franchis, shevardnadz, sordid, anti-ballist, antarct, submarin, chemical-weapon, premium, strident, gruesom, gape, obduraci, unrepres, reactor, drug-rel, gorbachev, nuclear-arm 
    ##  Topic 10: interfaith, ossetia, transbord, srgjan, kerim, sixty-second, abkhazia, sixty-third, war”, sixty-fourth, sixty-fifth, caucasus, sixty-sixth, post-conflict, georgia, results-ori, caspian, bucharest, miguel, future” 
    ##  Topic 11: countries-, rainforest, lender, lester, pharmaceut, deregul, plata, monopolist, cheap, attenu, oil-produc, outflow, rice, reinvest, specul, cook, gold, bankrupt, bought, expropri 
    ##  Topic 12: microcredit, ibero-american, multilingu, uruguayan, ortega, revolucionaria, biennium, clone, paz, cross-cut, money-laund, america’, bicess, bachelet, michell, xenophob, gender-bas, ghali, government’, carlo 
    ##  Topic 13: summit’, freedom”, system-wid, sergio, mello, qaeda, change”, quartet, vieira, monuc, monterrey, quartet’, katrina, national, counter-terror, ping, protect”, beslan, fifty-ninth, darfur 
    ##  Topic 14: buddhist, kyi, suu, aung, gay, quota-fre, intra-st, burma, agenda”, decommiss, replic, builder, priorit, smart, mdg, obscen, gender-bas, oblivi, consensus-build, heroin 
    ##  Topic 15: bulgaria, bulgarian, vanc, yeltsin, amara, xenophob, unprofor, ayala, pan-european, essi, unosom, untac, lasso, yugoslavia, croat, cleansing”, forty-eighth, “ethnic, croatia, post-cold-war 
    ##  Topic 16: country—, coun¬tri, inter¬n, nonalign, superpow, justice-lov, nonnuclear, nonaggress, brunei, kampuchea, kampuchean, invas, darussalam, powder, southeast, malvina, imr, illueca, contadora, deceit 
    ##  Topic 17: anti-apartheid, tela, pitiless, nkomati, sahraoui, reforest, debt-serv, gbadolit, azania, attenu, détent, perez, chirac, florin, cuellar, anc, indebted, reschedul, soviet-american, maghreb 
    ##  Topic 18: bashar, al-assad, isil, islamophobia, al-qaida, europe’, behead, qaeda, “never, borderless, al-qadhafi, jihad, smash, sleep, imam, hama, one’, templ, monster, muslim 
    ##  Topic 19: gaol, wife, falkland, arra, scrap, oblivi, tamper, commentari, klerk, peace-keep, premium, human-resourc, hearten, decenc, daunt, arrear, elig, descent, withhold, spurn 
    ##  Topic 20: bi-commun, bicommun, turkish, cypriot, ankara, bi-zon, bizon, turkey, greek, cyprus, greec, ismat, versaill, makario, humayun, maltes, nicosia, demilitaris, statesmanlik, rashe 
    ##  Topic 21: prom, santiago, allend, encycl, s-vii, medit, nehru, reformul, cross-road, food-stuff, indissolubl, sociolog, disenchant, lopez, inter¬n, pro-gramm, dialog, oligarchi, jurist, detr 
    ##  Topic 22: â€”, rapid-react, standbi, icc, srebrenica, peace-build, century”, peoples”, finland, landmin, anti-personnel, system’, robinson, clearanc, academia, “agenda, demin, commission’, nuclear-test, swedish 
    ##  Topic 23: aadd, s-vii, -stand, owen, acp, unifil, self-reli, mid-term, eec, undp, oecd, test-ban, hygien, whilst, plutonium, brandt, nuclear-weapon-fre, resettl, plea, -secretary-gener 
    ##  Topic 24: world-, rhodesia, nations-, -develop, salisburi, rhodesian, inter-depend, statesmanlik, british, balance-sheet, courtesi, short-com, spokesmen, commentari, postwar, time-t, indochina, tempo, behavior, sinai 
    ##  
    ##  Covariate Words:
    ##  Group 0: overwhelm, current, resolv, observ, inculc, expedit, skil, consequ, provid, laud, implement, similar, propon, enshrin, month, inconsist, taken, due, confid, outstand 
    ##  Group 1: autumn, centenni, maltreat, european, van, nutshel, inward, colleagu, harsher, underlin, duchi, everyday, censorship, outward, stricter, underestim, asymmetr, high-prior, insert, appal 
    ##  
    ##  Topic-Covariate Interactions:
    ##  Topic 1, Group 0: presidium, ssr, binari, jong, soviet-unit, byelorussian, anti-satellit, leonid, vladivostok, soviet-american, ukrainian, mongolian, romanian, leninist, counterrevolutionari, romania, bulgarian, bulgaria, hungarian, neutron 
    ##  Topic 1, Group 1: semi-manufactur, oil-import, saniti, ghast, free-market, riidig, debt-serv, fluctuat, skin, mitterrand, aberr, purest, dar, opec, expuls, versaill, egot, fidel, nigerian, steal 
    ##  
    ##  Topic 2, Group 0: nepales, singy, jigm, wangchuck, surinam, nepal, deregul, bhutan, kathmandu, china’, non-reciproc, punta, jamaica, etho, debt-serv, est, reschedul, semi-manufactur, debt-relief, gnp 
    ##  Topic 2, Group 1: food-stuff, burma, ivori, virtuous, amar, internet, freita, lobbi, czechoslovakia, buy, week’, rice, pump, oxygen, sell, organis, forgiv, safer, groundbreak, union’ 
    ##  
    ##  Topic 3, Group 0: tsetung, fretilin, vorster, independencia, sandinist, yanke, houari, agostinho, zionist, albania, gamal, neto, turnhall, paigc, partido, frelimo, reconquest, proletarian, sharpevill, albanian 
    ##  Topic 3, Group 1: unmitig, addl, vladivostok, aadd, stanislaw, trepczynski, nine, el-sadat, acrimoni, plutonium, hijack, nation-st, delimit, sinai, oil-export, comparison, sect, nicosia, steril, iaea 
    ##  
    ##  Topic 4, Group 0: forty-sixth, iceland, georgian, georgia’, malta, iraq-kuwait, forty-seventh, francoi, shorter-rang, reykjavik, ganev, arthur, ivan, rajiv, states-soviet, institutionalis, entent, samir, forty-third, intermediate-rang 
    ##  Topic 4, Group 1: fast-track, kurdish, hitler, saddam, misde, myth, lenin, digit, internet, shout, kazakhstan, shameless, fifty-eighth, demon, phantom, mercosur, antarctica, entrepreneur, cis, jona 
    ##  
    ##  Topic 5, Group 0: deir, azerbaijan’, armenian, azerbaijani, armenia, azerbaijan, lebanon’, flimsi, unifil, lebanes, sharon, zionist, tripoli, residenti, libyan, beirut, fez, bekaa, artilleri, jamahiriya 
    ##  Topic 5, Group 1: crimea, minsk, daesh, russia’, ukrain, seventieth, abkhazia, vuk, lakhdar, syria’, georgian, jeremić, georgia’, rule-bas, one’, separatist, sixty-seventh, ossetia, journalist, osc 
    ##  
    ##  Topic 6, Group 0: post-kyoto, ncds, sid, acidif, unreport, aosi, kitt, coral, montserrat, barbado, taiwan’, tromelin, rainforest, dominica, tobago, arthur, terrestri, minustah, barbuda, trinidad 
    ##  Topic 6, Group 1: state-build, kosovo’, lithuania, malian, ukraine’, pakistan’, malta, finland, afghani, hammarskjöld, afghanistan’, abdullah, sweden, ukrainian, mali, iran’, maltes, rabat, monrovia, koran 
    ##  
    ##  Topic 7, Group 0: monuc, al-bashir, eritrean, ecomog, bicess, liberian, ethiopia’, jona, somalia’, taylor, leonean, igad, burundi, al-shabaab, eritrea, inter-congoles, ethiopian, sierra, leon, unita 
    ##  Topic 7, Group 1: ireland, unionist, irish, etho, england, disinherit, sombr, framer, nationalist, africa—, northern, unifil, divin, slow-, pound, malign, mahatma, test-ban, paramilitari, devolv 
    ##  
    ##  Topic 8, Group 0: egypt’, tunb, gcc, abidin, yemen’, land--peac, zine, hamad, fahd, moussa, hebron, sultan, emir, hashemit, kuwait’, musa, afghani, yemeni, abdullah, tunisia 
    ##  Topic 8, Group 1: portuguese-speak, portug, ibero-american, portugues, bicess, non-self-govern, timores, unita, mozambican, timor, guinea-bissau, angolan, renamo, lisbon, timor-lest, chissano, “agenda, guido, biennium, future” 
    ##  
    ##  Topic 9, Group 0: taliban, lankan, pakistan’, cordovez, rahman, tamil, pakistani, kashmir, kashmiri, kabul, afghanistan’, saarc, islamabad, jammu, pakistan, bhutto, jawaharl, qaeda, buddhist, rajiv 
    ##  Topic 9, Group 1: churchil, falkland, argentin, renamo, cocain, chissano, ploy, britain, venezuelan, nkomati, glasnost, untag, sadcc, reschedul, colombian, unmanag, frenet, railway, reagan, perestroika 
    ##  
    ##  Topic 10, Group 0: ukraine’, cis, eurasian, kazakhstan, tajikistan, uzbekistan, belarus, aral, semipalatinsk, post-soviet, kyrgyz, russia’, silk, osc, minsk, ukrainian, karabakh, turkmenistan, tajik, mongolia 
    ##  Topic 10, Group 1: slovakia, romania, slovak, itali, francophoni, romanian, czech, bamako, italian, sixtieth, poland, oscar, pristina, balkan, beneficiari, priorit, haya, al-khalifa, torrenti, rome 
    ##  
    ##  Topic 11, Group 0: cereal, oil-export, volta, food-stuff, semi-manufactur, neoliber, locust, telephon, oil-import, freight, argentina’, trickl, consumer, textil, camera, opec, saniti, hydrocarbon, cocoa, underemploy 
    ##  Topic 11, Group 1: pittsburgh, music, arthur, anti-satellit, portillo, brazil’, dioxid, kissing, luther, bolivarian, equilibrium, lula, benit, kyoto, abraham, ozon, temperatur, recrudesc, emiss, communism 
    ##  
    ##  Topic 12, Group 0: mercosur, brazil’, cocain, coca, zelaya, salvadoran, monaco, marino, cuba’, haitian, chávez, argentina’, inter-american, colombian, peruvian, lula, andean, brasilia, paraguayan, manuel 
    ##  Topic 12, Group 1: gibraltar, spanish, spain, belgium, monuc, inter-congoles, congoles, sooth, maghreb, saharan, nagorni, patern, civilis, belgian, congo, sordid, unita, unfpa, brahimi, moroccan 
    ##  
    ##  Topic 13, Group 0: nepad, sahelo-saharan, ticad, kerim, ezulwini, japan’, mdgs, almati, hiv, antiretrovir, malian, blais, srgjan, deiss, haram, boko, sixty-fifth, francophoni, respiratori, mali 
    ##  Topic 13, Group 1: post-kyoto, lebanon’, hungari, islamabad, amman, taliban, curriculum, hungarian, kosovo, re-launch, congoles, ahtisaari, opium, balkan, luxembourg, al-shabaab, myanmar, aviv, neo, maldiv 
    ##  
    ##  Topic 14, Group 0: lykketoft, fiji’, myanmar’, un-women, kutesa, ebola, post-, myanmar, interfaith, andorra, women’, jeremić, al-nass, “bring, state-build, stakehold, ldcs, seventieth, driver, anti-corrupt 
    ##  Topic 14, Group 1: mitchel, ireland, lankan, irish, telephon, abba, vientian, tamil, somalia’, robinson, britain, landmin, diamond, hiv, union-unit, haemorrhag, sanctuari, gratuit, holkeri, fifty-sixth 
    ##  
    ##  Topic 15, Group 0: kosovo’, macedonian, slovakia, moldova, turkey’, albanian, srebrenica, romanian, kosovo, romania, bori, hungari, eurasia, hungarian, multi-religi, inter-ethn, rapid-react, transbord, turkey, croatian 
    ##  Topic 15, Group 1: hebron, cfa, indo, cordovez, bangui, anti-personnel, secretariat’, mercosur, sadc, klerk, eurasian, bongo, pere, bangkok, somalia’, beij, france’, salvadorian, tardi, tajikistan 
    ##  
    ##  Topic 16, Group 0: vientian, penh, phnom, thai, hanoi, mekong, indo-chines, minh, samdech, lao, indo, chi, laotian, lackey, lon, nol, buddhist, traitor, indochina, thailand 
    ##  Topic 16, Group 1: fez, ghetto, northsouth, bolivar, rancor, ida, polish, grudg, williamsburg, falkland, simon, beirut, cancun, nonprolifer, intermediate-rang, venic, icao, christoph, vanuatu, thirty-seventh 
    ##  
    ##  Topic 17, Group 0: cfa, bongo, eyadema, biya, anjouan, ndjamena, senegales, bamako, togoles, hadj, abdou, bangui, niger, rwandes, benin, togo, comorian, comoro, idriss, zair 
    ##  Topic 17, Group 1: punta, sadcc, est, sharpevill, twelv, mururoa, terrestri, roh, untag, states-soviet, debt-servic, del, argentina’, cordovez, shorter-rang, security-build, growth-ori, isthmus, inf, amazon 
    ##  
    ##  Topic 18, Group 0: song, koran, jesus, music, theolog, muhammad, allah, boot, america’, hitler, telephon, divin, bibl, hebrew, camera, sweet, mecca, vladimir, pogrom, christ 
    ##  Topic 18, Group 1: daesh, geolog, deir, interfaith, egypt’, ebola, silk, pristina, abdullah, afghanistan’, redraw, france’, faso, burkina, belarus, insurg, climate-chang, taliban, lykketoft, stewardship 
    ##  
    ##  Topic 19, Group 0: sadcc, lesotho, swazi, gambian, swaziland, renamo, malawi, botha, mozambican, banjul, untag, gambia, chissano, nkomati, unmitig, mpla, turnhall, anti-apartheid, zambian, pac 
    ##  Topic 19, Group 1: palac, unprofor, netherland, bosnian, edvard, intrigu, builder, tiger, glass, politic, australian, jump, bori, chechnya, peace—, chairperson, supervisori, recrudesc, icrc, revitalis 
    ##  
    ##  Topic 20, Group 0: tyrol, short-com, cordovez, fez, prom, burma, williamsburg, s-vii, coun¬tri, qud, country—, kampuchea, austrian, mojsov, imr, shirley, hamilton, lievano, choudhuri, wechmar 
    ##  Topic 20, Group 1: turkey’, landslid, hydrocarbon, quito, win-win, nautic, albanian, olymp, â€”, ali, uninhabit, truce, balkan, athen, fahd, reunifi, peruvian, plunder, sixty-sixth, shelf 
    ##  
    ##  Topic 21, Group 0: argentin, inter-ocean, montevideo, torrijo, ecla, uruguayan, quito, isthmus, panamanian, peruvian, portillo, bolivian, bolivar, honduran, herrera, paz, gibraltar, venezuelan, plata, paraguayan 
    ##  Topic 21, Group 1: roger, aaddl, belgium, senghor, thant, -popul, hambro, malik, franc, root-caus, mobutu, jar, leonid, presidium, indo-chines, addl, entent, rahman, italian, aadd 
    ##  
    ##  Topic 22, Group 0: ghali, amara, diogo, essi, liechtenstein, amar, post-cold-war, freita, “renew, australia’, canadian, reform”, boutro, boutros-ghali, “never, lester, oil--food, norwegian, forty-ninth, peace-keep 
    ##  Topic 22, Group 1: austria, latvia, austrian, decades-long, pogrom, slovenia, tyrol, al-bashir, stomach, juvenil, residenti, baltic, macedonian, poppi, thabo, extrajudici, smuggl, anti-corrupt, ecomog, mano 
    ##  
    ##  Topic 23, Group 0: australian, zealand, bougainvill, distant-wat, polynesia, tokelau, niue, matignon, melanesian, nguema, mbasogo, kanak, guinea’, fijian, atol, mururoa, caledonia, palau, tuna, fiji 
    ##  Topic 23, Group 1: mekong, danish, netherland, longterm, nordic, botha, denmark, quarter-centuri, surinam, biko, xxvii, centrifug, anti-satellit, xxv, connexion, secretarygener, sahelian, nonprolifer, standard-set, dam 
    ##  
    ##  Topic 24, Group 0: aaddl, aadd, addl, hambro, thant, edvard, stanislaw, trepczynski, uthant, jar, unctadj, xxv, benit, malik, freight, peke, kissing, roger, hie, quarter-centuri 
    ##  Topic 24, Group 1: flimsi, anti-apartheid, mojsov, unifil, meagr, jobless, non-nuclear-weapon, grotesqu, botswana, transkei, zimbabw, demilitar, zimbabwean, resid, hatch, build-, anglo-american, round-tabl, david, modem 
    ##
