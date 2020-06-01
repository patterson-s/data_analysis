``` r
pacman::p_load(stm,dplyr,quanteda,readr,ggplot2,stargazer)
set.seed(42)

load("C:/Users/spatt/OneDrive - McGill University/patterson_pouliot/inequality/inequality/interaction_k30.RDATA")
```

``` r
# Manual Inspection of Words 
labelTopics(interaction_k30, n = 10)
```

    ## Topic 1 Top Words:
    ##       Highest Prob: state, nuclear, peac, intern, unit, peopl, weapon, nation, soviet, countri 
    ##       FREX: soviet, poland, socialist, detent, nuclear, prohibit, disarma, weapon, race, mongolian 
    ##       Lift: binari, ilyich, songun, soviet-indian, space-bas, ssr, ceausescu, jaruzelski, shcherbitski, soviet-french 
    ##       Score: soviet, co-oper, ssr, mongolian, detent, romania, poland, nuclear, socialist, byelorussian 
    ## Topic 2 Top Words:
    ##       Highest Prob: develop, nation, global, climat, chang, unit, sustain, intern, challeng, secur 
    ##       FREX: mdgs, post-, climat, emiss, ki-moon, theme, sid, green, high-level, mitig 
    ##       Lift: -track, “effect, post-kyoto, redd-plus, treki’, bhutan’, poznan, mdg, “transform, sendai 
    ##       Score: mdgs, post-, ki-moon, sid, peacebuild, millennium, global, emiss, mdg, develop 
    ## Topic 3 Top Words:
    ##       Highest Prob: peopl, countri, state, unit, aggress, struggl, independ, nation, world, forc 
    ##       FREX: imperialist, imperi, revolutionari, reactionari, fascist, colonialist, cuban, expansionist, aggress, capitalist 
    ##       Lift: anti-imperi, battambang, glorieus, hoxha, social-imperi, social-imperialist, tonkin, enver, imperialist-zionist, cia 
    ##       Score: imperialist, imperi, zionist, kampuchea, viet, albania, vietnames, nam, aggress, reactionari 
    ## Topic 4 Top Words:
    ##       Highest Prob: unit, nation, secur, human, right, council, must, intern, member, organ 
    ##       FREX: oper, peacekeep, canada, non-prolifer, personnel, court, peace-keep, humanitarian, finland, council 
    ##       Lift: ahern, berti, taoiseach, subsidiar, mulroney, canadian, swedish, robinson, olara, finland 
    ##       Score: peace-keep, peacekeep, unit, finland, landmin, nuclear, nation, canada, council, canadian 
    ## Topic 5 Top Words:
    ##       Highest Prob: intern, develop, econom, countri, world, must, new, polit, problem, nation 
    ##       FREX: interdepend, structur, adjust, imbal, technolog, balanc, trend, factor, consensus, concept 
    ##       Lift: energy-defici, one—, figueiredo, post-industri, sarney, laissez-fair, deflationari, unpromis, raw-material-produc, punta 
    ##       Score: co-oper, develop, econom, intern, global, interdepend, debt, industri, uruguay, gatt 
    ## Topic 6 Top Words:
    ##       Highest Prob: countri, african, peac, intern, africa, nation, republ, state, govern, organ 
    ##       FREX: chad, burundi, niger, mali, rwanda, congo, burkina, equatori, faso, gabon 
    ##       Lift: amadou, faso, idriss, mali’, mbasogo, niger’, abdoulay, ange-félix, anjouan, bata 
    ##       Score: burundi, niger, mali, chad, guinea, benin, rwanda, equatori, togo, burkina 
    ## Topic 7 Top Words:
    ##       Highest Prob: intern, secur, state, countri, peac, region, iraq, unit, peopl, nation 
    ##       FREX: iraqi, iraq, yemen, kuwait, islam, emir, gulf, tunisia, morocco, iranian 
    ##       Lift: abdrabuh, abidin, alija, bab, emirati, hamad, mousa, omani, tunb, al-jab 
    ##       Score: arab, iraq, kuwait, islam, iraqi, yemen, emir, iran, morocco, oman 
    ## Topic 8 Top Words:
    ##       Highest Prob: israel, peac, arab, palestinian, isra, lebanon, peopl, state, nation, east 
    ##       FREX: israel, egypt, isra, jordan, lebanon, jerusalem, lebanes, arab, palestinian, jewish 
    ##       Lift: judaea, judea, mosh, samaria, zion, dayan, irgun, yasin, kippur, yom 
    ##       Score: arab, israel, zionist, lebanon, isra, palestinian, lebanes, jordan, egypt, jerusalem 
    ## Topic 9 Top Words:
    ##       Highest Prob: africa, south, countri, develop, intern, econom, african, peopl, nation, namibia 
    ##       FREX: zimbabw, namibia, racist, apartheid, white, southern, smith, africa, south, black 
    ##       Lift: fswapoj, turnhall, transkei, self-extinct, muzorewa, mogadiscio, swapoj, anglo, farah, supremacist 
    ##       Score: zimbabw, racist, rhodesia, namibia, co-oper, africa, apartheid, smith, vorster, swapo 
    ## Topic 10 Top Words:
    ##       Highest Prob: nation, unit, develop, will, world, problem, peac, hope, organ, govern 
    ##       FREX: bangladesh, viet-nam, twenty-fifth, program, neighbor, endeavor, xxv, dialog, thant, honor 
    ##       Lift: addlj, counter-accus, edvard, non-arma, tanaka, hambro, schumann, brooksrandolph, hard-cor, alec 
    ##       Score: viet-nam, co-oper, dialog, connexion, rhodesia, bangladesh, xxv, endeavor, neighbor, sea-b 
    ## Topic 11 Top Words:
    ##       Highest Prob: will, communiti, european, right, cyprus, govern, effort, europ, problem, human 
    ##       FREX: ireland, turkish, cyprus, turkey, malta, austria, cypriot, greec, greek, mediterranean 
    ##       Lift: famagusta, ankara, austro-italian, bizon, denktash, ellemann-jensen, partitionist, turkish-cypriot, varosha, cyprus’ 
    ##       Score: turkish, co-oper, malta, turkey, cyprus, ireland, cypriot, greec, greek, mediterranean 
    ## Topic 12 Top Words:
    ##       Highest Prob: terror, afghanistan, peopl, govern, pakistan, terrorist, countri, india, will, forc 
    ##       FREX: pakistan, sri, lanka, kashmir, india, taliban, afghan, afghanistan, muslim, kabul 
    ##       Lift: benazir, jirga, ltte, pakistan’, tamil, inter-servic, jirgah, loya, ranger, lankan 
    ##       Score: pakistan, taliban, afghanistan, sri, lanka, afghan, islam, kashmir, muslim, india 
    ## Topic 13 Top Words:
    ##       Highest Prob: nation, develop, unit, peac, world, intern, will, organ, cooper, econom 
    ##       FREX: fiftieth, nepal, forty-eighth, myanmar, boutro, boutros-ghali, swaziland, peace-keep, cold, rio 
    ##       Lift: indlovukazi, lumbini, mswati, swazi, yasushi, nepal’, midrand, seven-step, akashi, mindanao 
    ##       Score: myanmar, bosnia, nepal, forty-eighth, boutro, herzegovina, boutros-ghali, swaziland, peace-keep, freita 
    ## Topic 14 Top Words:
    ##       Highest Prob: peopl, countri, will, intern, world, nation, organ, peac, must, problem 
    ##       FREX: portugues, portug, verd, cape, algeria, zair, mauritania, sahara, raw, sao 
    ##       Lift: pereira, volta, interpenetr, lamizana, sangoul, mondlan, seyni, sedar, bokassa, tarfaya 
    ##       Score: co-oper, volta, zair, dialog, portugues, verd, mauritania, oau, portug, favor 
    ## Topic 15 Top Words:
    ##       Highest Prob: peac, africa, african, govern, nation, intern, countri, communiti, unit, conflict 
    ##       FREX: sierra, ethiopia, leon, uganda, liberia, sudan, somalia, somali, eritrea, kenya 
    ##       Lift: eritrea’, ethiopia’, igad, museveni, tanzania’, unme, eritrean, badm, eritrea-ethiopia, kabbah 
    ##       Score: somalia, sudan, sierra, uganda, leon, ethiopia, somali, liberia, igad, ecowa 
    ## Topic 16 Top Words:
    ##       Highest Prob: will, can, one, must, world, now, year, time, mani, new 
    ##       FREX: think, want, know, franc, say, thing, perhap, someth, said, happen 
    ##       Lift: bach, néstor, deutsch, kirchner, amia, sleepless, shorthand, asociación, israelita, guy 
    ##       Score: can, franc, want, must, one, know, let, now, say, europ 
    ## Topic 17 Top Words:
    ##       Highest Prob: develop, nation, unit, intern, secur, terror, global, will, peac, must 
    ##       FREX: millennium, annan, kofi, hivaid, terror, summit, partnership, sixtieth, terrorist, johannesburg 
    ##       Lift: mello, ping, vieira, arms”, baku-tbilisi-ceyhan, seung, soo, seung-soo, kavan, lindh 
    ##       Score: hivaid, millennium, annan, kofi, nepad, monterrey, peacebuild, darfur, terror, doha 
    ## Topic 18 Top Words:
    ##       Highest Prob: island, nation, pacif, new, unit, state, govern, region, small, countri 
    ##       FREX: zealand, fiji, papua, australia, pacif, solomon, iceland, caledonia, fish, island 
    ##       Lift: maori, matignon, fiji’, zealand, auckland, biketawa, distant-wat, drift-net, evatt, fiji 
    ##       Score: fiji, papua, zealand, solomon, island, pacif, samoa, iceland, australia, caledonia 
    ## Topic 19 Top Words:
    ##       Highest Prob: nation, unit, peac, develop, will, intern, countri, hope, south, peopl 
    ##       FREX: organis, malawi, liberian, cuellar, javier, forty-third, gulf, forty-fourth, forty-sixth, cease-fir 
    ##       Lift: mobilis, afonso, dlvoir, hunan, jeopardis, koevoet, marginalis, npfl, renamo, ulimo 
    ##       Score: malawi, liberian, kuwait, cuellar, organis, forty-third, forty-sixth, caputo, forty-fourth, drug 
    ## Topic 20 Top Words:
    ##       Highest Prob: intern, will, human, nation, right, countri, social, organ, develop, new 
    ##       FREX: traffick, democraci, societi, drug, san, uruguay, spain, marino, brazil, mexico 
    ##       Lift: chile’, mendoza, mitch, monaco’, rainier, spain’, instraw, leonel, peru’, paraguay’ 
    ##       Score: marino, drug, monaco, andorra, traffick, millennium, mercosur, democraci, uruguay, spain 
    ## Topic 21 Top Words:
    ##       Highest Prob: peac, peopl, will, must, nation, world, right, secur, unit, intern 
    ##       FREX: syria, apv, syrian, seventieth, two-stat, extremist, iran’, humankind, libya, girl 
    ##       Lift: al-assad’, bisexu, bokova, irina, lesbian, paralymp, tahrir, transgend, isil, ashton 
    ##       Score: syria, syrian, ebola, isil, iran’, two-stat, timor-lest, ki-moon, syria’, world’ 
    ## Topic 22 Top Words:
    ##       Highest Prob: countri, develop, per, cent, world, econom, product, economi, trade, increas 
    ##       FREX: cent, per, rate, agricultur, incom, billion, oil, product, price, export 
    ##       Lift: bangla, bangabandhu, -five, cent, per, tariff-fre, potato, non-oil, metric, averag 
    ##       Score: per, cent, develop, countri, debt, product, oil, food, market, price 
    ## Topic 23 Top Words:
    ##       Highest Prob: nation, intern, unit, region, european, countri, secur, state, republ, cooper 
    ##       FREX: croatia, azerbaijan, moldova, armenia, herzegovina, bosnia, georgia, latvia, kosovo, macedonia 
    ##       Lift: albania’, armenia’, azerbaijani, bulgaria’, herzegovina’, icti, moldova, republika, slovenian, armenian-azerbaijani 
    ##       Score: croatia, azerbaijan, herzegovina, bosnia, moldova, albania, armenia, latvia, slovakia, osc 
    ## Topic 24 Top Words:
    ##       Highest Prob: nation, unit, intern, state, region, japan, countri, secur, world, will 
    ##       FREX: kazakhstan, tajikistan, belarus, japan, ukrain, turkmenistan, kyrgyzstan, mongolia, uzbekistan, russia 
    ##       Lift: cica, kazakstan, kyrgyzstan, kyrgyzstan’, nazarbaev, niyazov, nursultan, aral, kazakhstan, kyrgyz 
    ##       Score: belarus, tajikistan, kazakhstan, turkmenistan, mongolia, ukrain, kyrgyzstan, uzbekistan, kyrgyz, japan 
    ## Topic 25 Top Words:
    ##       Highest Prob: intern, countri, peac, nation, unit, peopl, continu, state, south, develop 
    ##       FREX: namibian, fortieth, kampuchea, pretoria, namibia, withdraw, plo, contadora, co-oper, race 
    ##       Lift: conse¬qu, oo-oper, pinié, organi¬z, situa¬t, solu¬t, occupa¬t, inde¬pend, mem¬ber, devel¬op 
    ##       Score: co-oper, kampuchea, contadora, namibian, dialog, afghanistan, nonalign, kampuchean, pretoria, namibia 
    ## Topic 26 Top Words:
    ##       Highest Prob: nation, world, human, peopl, unit, right, war, power, state, one 
    ##       FREX: man, god, dream, earth, love, moral, ethic, beauti, soul, spiritu 
    ##       Lift: monoth, psychic, saviour, pang, lunat, discomfort, theolog, unidentifi, largess, infin 
    ##       Score: human, man, world, god, nation, war, right, power, divin, peopl 
    ## Topic 27 Top Words:
    ##       Highest Prob: countri, nation, peac, develop, unit, intern, will, republ, world, korea 
    ##       FREX: asean, thailand, lao, viet, nam, south-east, korea, korean, cambodia, peninsula 
    ##       Lift: nam’, jong, thai, political-secur, surinames, jung, thailand, mekong, asean, kim 
    ##       Score: viet, lao, nam, thailand, asean, kampuchea, vietnames, kampuchean, cambodia, thai 
    ## Topic 28 Top Words:
    ##       Highest Prob: nation, intern, state, unit, countri, general, assembl, right, will, principl 
    ##       FREX: sea, jurisdict, item, articl, law, spain, subject, coastal, text, procedur 
    ##       Lift: vina, sakiet, trawler, velasco, possideti, gonzalez, width, xxiii, uti, echeverria 
    ##       Score: co-oper, sea-b, connexion, favor, sea, spain, gibraltar, waldheim, spanish, coloni 
    ## Topic 29 Top Words:
    ##       Highest Prob: state, develop, caribbean, small, nation, countri, govern, intern, econom, unit 
    ##       FREX: tobago, trinidad, bahama, caribbean, barbado, saint, haiti, caricom, jamaica, haitian 
    ##       Lift: dominica, bahamian, banana-produc, barbados’, belize’, carib, dominica’, grenada’, kitt, lucia’ 
    ##       Score: tobago, barbado, trinidad, bahama, caricom, grenada, dominica, kitt, caribbean, haiti 
    ## Topic 30 Top Words:
    ##       Highest Prob: peac, govern, countri, america, peopl, american, latin, state, will, nation 
    ##       FREX: costa, bolivia, rica, panama, guatemala, ecuador, peru, hondura, argentina, venezuela 
    ##       Lift: guatemalan, bolívar, campin, celac, chamorro, inter-ocean, juarez, nicolá, saavedra, simón 
    ##       Score: panama, bolivia, paraguay, ecuador, costa, rica, guatemala, hondura, panamanian, bolivian

``` r
# Topic Proportions 
plot(interaction_k30,type = "summary", custom.labels = "",par(bty="n",col="grey40",lwd=5))
```

![](ik30analysis_files/figure-markdown_github/labelTopics%20i_k30-1.png)
