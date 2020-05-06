Më thuaj ku të shkoj - Koordinata dhe drejtimi
=================================================

.. include:: blocks.txt

.. include:: icons.txt

.. infonote::

  |intro2|


Pasi të njihni bazat e mjedisit, është koha të mësoni se si mund t'i dërgoni sprites tuaj në vendin e dëshiruar në skenë. Për ta bërë atë, duhet të dini se si organizohet faza dhe cilat komanda mundësojnë lëvizjen.

.. sidebar:: Sprite Coordinates

 |stage|

.. |stage| image:: ../_images/2/fig2_1.png

.. topic:: Skena
      
 Kur hapni Scratch, skena krijohet automatikisht: një drejtkëndësh i bardhë 480 pika i gjerë dhe 360 pika i lartë. Pika më e vogël që mund të shfaqet në një ekran grafik kompjuterik quhet *Pixel*.

  Skena është aty ku do të zhvillojnë tregimet, lojërat dhe animacionet tuaja. Shtë i palëvizshëm, si një akuariumi, por banorët e tij - Sprites janë gjithmonë në lëvizje dhe bashkëveprojnë me njëri-tjetrin. Për të kontrolluar me lehtësi lëvizjet e sprites, secilës vend në skenë i është caktuar një adresë - *koordinatat x dhe y*, këto koordinata paraqesin distancën e asaj vendi të veçantë nga qendra e skenës. Pika, e cila është e vendosur në qendër të fazës ka koordinatat х = 0 dhe у = 0, ose (0,0).

  Koordinatat na lejojnë të lëvizim me saktësi sprites tonë nëpër skenë dhe t'i pozicionojmë ato kudo që dëshirojmë (x, y). Pozicioni aktual i sprite mund të shihet në informacionin aktiv të sprite. 


.. topic:: Funksionet e blloqeve *Motion*
 
 Të gjitha komandat, të cilat mundësojnë pozicionimin e sprite në vendin e dëshiruar dhe kontrollojnë drejtimin dhe lëvizjen e tij, janë të vendosura në grupin e blloqeve të quajtur *lëvizja*. Në këtë mësim, ju do të mësoni më shumë rreth blloqeve të lëvizjes dhe si të përdorni **blloqet e reportazheve**, duke parë shembuj dhe duke bërë ushtrime. Blloqet e reporterëve nuk korrespondojnë me komandat gjuhësore, dhe ato nuk mund të qëndrojnë në mënyrë të pavarur në një skenar. Funksioni i një blloku reporterësh nga grupi *Motion* është ruajtja e koordinatave dhe udhëzimeve aktuale të Sprites.

.. topic:: Motion Reporters

 Në këtë grup ekzistojnë blloqet |x_position| dhe |y_position|, të cilat përmbajnë informacionin aktual për pozicionin e sprite (koordinatat e tij x dhe y), dhe bllokun |direction|, i cili paraqet drejtimin e sprite.

  Nëse doni të shihni koordinatat aktuale dhe drejtimin e sprite, duhet të klikoni në kutinë e kontrollit ngjitur me bllokun e dëshiruar. Nëse klikoni në kutitë e kontrollit pranë reporterëve të lëvizjes, ekranet me të cilat mund të monitoroni koordinatat aktuale dhe drejtimin e sprite do të shfaqen në skenë.
 
 .. image:: ../_images/2/fig2_2.png
   :width: 400px   
   :align: center
 
 
.. topic:: Lëvizja relative dhe absolute

  Ju mund të dërgoni spriten tuaj në një vend të veçantë në skenë në dy mënyra të ndryshme: me lëvizje absolute ose relative.

  **Lëvizja Absolute** është duke lëvizur në një vend - destinacion specifik, pavarësisht nga pozicioni aktual i sprite.

  Në Scratch ju mund ta dërgoni sprite tuaj në një pozicion të caktuar (х, у) në skenë, domethënë, ju mund të kryeni lëvizje absolute duke përdorur blloqet e mëposhtme:

  - |goto_xy| - shkoni në pozicionin (х, у),
  - |glide_xy| - rrëshqisni në pozicionin (х, у),
  - |set_x| - vendosni koordinatën x në pozicion,
  - |set_y|  - vendosni koordinatën y në pozicion.

 duke përdorur bllokun |goto_xy| i sprite do të lëvizë menjëherë në pozicionin e dhënë (х, у).

 Në mënyrë të ngjashme, objektivi do të arrihet me bllokun |glide_xy|, por masa nuk do të ishte e menjëhershme; do të zgjaste një numër i caktuar sekondash. Sa më i lartë të jetë numri i sekondave të dhëna, aq më shumë do t'i duhet spërkatjes për të arritur në destinacionin e saj.

 Një mënyrë tjetër për të vendosur një destinacion në lëvizje absolute është vendosja në mënyrë të pavarur e koordinatave x dhe y, duke përdorur blloqet |set_x| dhe |set_y|.

 **Lëvizja Relative** është duke lëvizur në një vend të përcaktuar nga numri i hapave që do të bëjë sprite nga pozicioni aktual. Sigurisht, ju gjithashtu duhet të vendosni drejtimin në të cilin duhet të lëvizë sprite (djathtas, lart, etj.).

 Një mënyrë tjetër për të vendosur një destinacion në lëvizje relative është të vendosni në mënyrë të pavarur koordinatat x dhe y, duke përdorur blloqet c hange_x| dhe |change_y|.

 Në Scratch, ju mund ta dërgoni sprite në një vend të përcaktuar nga numri i hapave nga pozicioni i tij aktual, domethënë, ju mund të kryeni lëvizje relative duke përdorur blloqet e mëposhtme:
 
 - |change_x| - zhvendosni një sasi të caktuar pikselash horizontalisht në lidhje me pozicionin aktual,
 - |change_y| - zhvendosni një sasi të caktuar pikselash vertikalisht në lidhje me pozicionin aktual (х, у),
 - |ana_right| - ktheni djathtas një sasi të caktuar shkallësh në lidhje me drejtimin aktual,
 - |ana_left| - ktheni majtas një sasi të caktuar shkallësh në lidhje me drejtimin aktual,
 - |move_steps| - lëvizni një sasi të caktuar hapash në drejtimin e dhënë në lidhje me pozicionin aktual.
    

.. sidebar::  Blloqet e drejtimit
   :subtitle: |point_direction| dhe |point_towards|

   Ekzistojnë tre mënyra për të vendosur një vlerë në fushën hyrëse të bllokut të parë:

   |direction1|

    (1) për të zgjedhur njërën prej vlerave të ofruara nga lista rënëse, për shembull (0) lart;
    (2) shkruani një vlerë të re, në vend të së vjetër, për shembull 45;
    (3) për të rrotulluar shigjetën blu që tregon drejtimin në informacionin aktual të Sprite.

    Nga lista e lëshimit mund të zgjidhni se cili objekt do të drejtohet Sprite në bllokun tjetër.

   |direction2|

.. |direction1| image:: ../_images/2/fig2_3.png

.. |direction2| image:: ../_images/2/fig2_4.png

.. topic:: Drejtimi dhe rrotullimi

 Përveç blloqeve të rrotullimit |kthesës_right| dhe |turn_left|, të cilat ju lejojnë të ndryshoni drejtimin në lidhje me drejtimin aktual të sprite, në Scratch, ekziston një mundësi për të përdorur blloqe që vendosin drejtimin pavarësisht nga pozicioni aktual i Sprite.

  Këto janë blloqet|point_direction| dhe |point_towards|.

  Në figurën e mëposhtme mund të gjeni vlerat kryesore të drejtimit të cilat mund të vendosni në fushën hyrëse të bllokut të parë: *lart* (Veri), *djathtas* (Lindje), *poshtë* (Jug) dhe *majtas* (Perëndim).

 .. image:: ../_images/2/fig2_5.png
   :width: 250px   
   :align: center

 Ju gjithashtu mund të vendosni vlera të tjera, për shembull, vlera 45 do të tregojë rrjedhën në drejtim të verilindjes, dhe 135 në juglindje. Për ta treguar atë në perëndim, nuk keni nevojë të përdorni numra negativë. Në vend të kësaj mund të shkruani numra nga 180 në 360.

  Blloku i dytë tregon pikën drejt një treguesi të miut ose drejt një avulli tjetër në projekt. Duke klikuar në trekëndëshin e bardhë në fushën e vlerës, ju mund të hapni listën rënëse dhe të zgjidhni se cili objekt dëshironi të tregoni burimin tuaj. Për shembull, në projektin "Shëtitje Dinosauri", i cili do të analizohet më vonë në këtë mësim, macja mund të drejtohet në drejtim të treguesit të miut ose drejt njërit prej tre dinosaurëve, të cilët përfaqësojnë sprita në këtë projekt.
  

|study| Studioni shembujt
------------------------------------

Ne kemi treguar mënyrën e thjeshtë për ta bërë fjalën tonë sprite në projektin tonë "Hello World", dhe pastaj duke bërë ushtrime të azhurnuar projektin tonë në mënyrë që sprite të shqiptojë vërtet tekstin, ne do të tregojmë tani komandat themelore të cilat do të na mundësojnë të lëvizim tonë, dhe pastaj ne do t'i përmirësojmë ato përmes ushtrimeve të ndryshme.

Shembulli 1 - Projekti "The Walk"
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


||1| Klikoni në blloqet *Motion*, dhe pastaj tërhiqni bllokun |move_steps| në Script Area dhe klikoni mbi të. Macja do të lëvizë 10 hapa djathtas.

|2| Klikoni disa herë në këtë bllok dhe çojeni mace në skajin e djathtë të ekranit.

Klikimi i përsëritur në bllokun e lëvizjes ka lejuar që veprimi i caktuar nga ky bllok, të përsëritet disa herë. Përsëritja e një veprimi të veçantë mund të arrihet edhe me kodim.

|3| Kthejeni macen në mes të ekranit dhe klikoni në blloqet *Control*. Blloqe në formë të ndryshme nga ato që keni përdorur do të shfaqen në Bleta Palette - blloqe në formë C me një "gojë" në të cilën mund të futni blloqe të tjera.

|4| Zgjidhni bllokun |forever| dhe tërhiqeni atë në Zonën e Shkrimeve. Duke klikuar në këtë bllok mundëson që të gjitha blloqet që janë futur në të të funksionojnë përgjithmonë (derisa të ndaloni ekzekutimin e programit duke klikuar në shenjën *stop*).

|5| Vendosni një bllok lëvizje në "gojën" e bllokut të përsëritur përgjithmonë dhe klikoni mbi ato. Macja do të dalë përsëri në ekran.

Ekziston një mënyrë për të mbajtur lëvizjen e sprite brenda kufijve të ekranit. Kjo do të ishte të përdorni bllokun me komandën *nëse në buzë, fryrje*. Ky bllok është i vendosur në blloqet *Motion*.

|6| Ndaloni ekzekutimin e blloqeve duke klikuar në shenjën *stop* dhe më pas tërhiqni bllokun |if_edge| në zonën e Skriptit dhe futeni në "gojën" e bllokut të përsëritur përgjithmonë, poshtë bllokut të lëvizjes.

.. sidebar:: Skripti iprojektit

    Shkrimi i mëposhtëm shtohet në spritein e maceve.

  |script|

.. |script| image:: ../_images/2/fig2_6.png

Duke drejtuar këtë skenar të ndryshuar, macja do të lëvizë vazhdimisht nga një skaj në tjetrin, por kur të zhvendoset në të majtë, do të përballet me mënyrën e gabuar. Sigurisht, ekziston një mënyrë për ta rregulluar këtë. Njëra është të ndryshoni mënyrën e lëvizjes së sprite në Informacionin Sprite, dhe tjetra është të përdorni një nga blloqet e rrotullimit.

|7| Zvarrit bllokun |rotacioni_style| nga blloqet *Motion* dhe vendoseni sipër bllokut të përsëritur përgjithmonë. Sigurohuni që mënyra e rrotullimit *majtas-djathtas* është zgjedhur nga lista dropdown e këtij blloku.

|8| Vendosni | klikuar_flag | bllok në krye të Script, dhe duke bërë këtë ju keni përfunduar projektin "Ecni".

Tani mund ta drejtoni projektin duke klikuar në *flamurin e gjelbër* dhe ta ndaloni duke klikuar në shenjën *stop*. Ruani projektin dhe vazhdoni të eksploroni.

.......

Në projektin tonë të ardhshëm, ne do të tregojmë se si ju mund të prezantoni sprites dhe sfondet e reja, dhe si të udhëzoni një sprite duke përdorur treguesin e miut. Prandaj, para se të kaloni në këtë shembull, shikoni mësimet *shtoni një Sprite* dhe *Shtoni një sfond*.

Shembulli 2 - "Dinosauri ecën"
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Në shembullin e mëparshëm, ne kemi përdorur bllokun ``forever`` për ta bërë që maceja e maces të lëvizë vazhdimisht midis skajeve të ekranit derisa të ndalojmë ekzekutimin e projektit duke klikuar në shenjën *stop*. Në këtë projekt, ne do të kemi katër sprites, dhe secila prej tyre do të ketë skriptet e tyre, të cilat do të përcaktojnë sjelljen e tyre. Macja do të ndjekë treguesin e miut përgjithmonë, dhe tre sprites e mbetura - dinosaurët, do të drejtohen përgjithmonë drejt maceve. Pamja e fazës në fillim të drejtimit të projektit është paraqitur në figurën vijuese.

.. image:: ../_images/2/fig2_7.png
   :width: 490px   
   :align: center

**Creation of the Project**

.. sidebar:: Selecting the Backdrop

  Në projektin tonë të ardhshëm, ne do të tregojmë se si ju mund të prezantoni sprites dhe sfondet e reja, dhe si të udhëzoni një sprite duke përdorur treguesin e miut. Prandaj, para se të kaloni në këtë shembull, shikoni mësimet * Shtoni një Sprite * dhe * Shtoni një sfond *.

Shembulli 2 - "Ecen Dinosauri"
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

** Krijimi i Projektit **

.. sidebar:: Zgjedhja e sfondit

  Ju mund të shtoni një sfond të ri në projekt duke klikuar ikonën e vendosur në të djathtë, ngjitur me ikonën Zgjidhni një Sprite, e cila përdoret për zgjedhjen e spritave të reja.

  |New_backdrop|

.. |new_backdrop| imazh :: ../_images/2/fig2_8.png


|1| Klikoni në ikonën për të zgjedhur sfondet dhe zgjidhni sfondin *Jurassic* nga biblioteka e prapavijës.

|2| Zgjidhni sprites *Dinosaur1*, *Dinosaur2* dhe *Dinosaur3* nga biblioteka e Sprites.

|3| Vendosni sprites tuaj si ato janë në figurën e mësipërme. Ju duhet të ndryshoni drejtimin e *Dinosaur2*. Vlera e paracaktuar e drejtimit për të gjitha sprites është 90: sup: `о` (ata po kërkojnë në të djathtë) dhe stili i tyre i rrotullimit është *Gjithë Rreth*. Të gjitha këto cilësime mund të ndryshohen në pjesën e informacionit Sprite ose duke përdorur blloqe të përshtatshme për të formuar skriptet që i shtohen një Sprite të veçantë. Në këtë projekt, ne do të përdorim opsionin e parë.

|4| Në dritaren e informacionit Sprite vendosni stilin e rrotullimit si më poshtë: *Dinosaur1* - *mos rrotullohet*, *Dinosaur2 * - *majtas / djathtas*, *Dinosaur3* - *All*.

|5| Të gjithë dinosaurët shtojnë të njëjtin skenar, i cili do t'i urdhërojë ata të drejtojnë drejt maceve gjatë drejtimit të të gjithë projektit. Sidoqoftë, ata do të sillen ndryshe sepse nuk kanë të njëjtin stil rotacioni në cilësimet e tyre të informacionit Sprite.
   
|6| Për sprite e maceve ju duhet të vendosni komandat, të cilat do t'i mundësojnë të drejtojnë drejt koordinatave të treguesit të miut, domethënë, të lëvizni nëpër skenë në të njëjtën mënyrë përdoruesi lëviz miun.

Skriptet që përshkruajnë sjelljen e dinosaurëve dhe maceve janë paraqitur në figurën vijuese.

.. image:: ../_images/2/fig2_9.png
   :width: 395px   
   :align: center
 
Drejtoni projektin dhe lëvizni miun në skenë. Vini re se dinosaurët janë duke ndjekur lëvizjet e saj në mënyra të ndryshme.

.......

.. sidebar:: Zgjedhja e çelësave

 Çelësi i tastierës që do të drejtojë skenarin zgjidhet duke klikuar në trekëndëshin e bardhë ngjitur me emrin e çelësit (hapësira) dhe më pas duke zgjedhur tastin e dëshiruar nga lista rënëse. 

  |fig2_11|

.. |fig2_11| image:: ../_images/2/fig2_10.png

Example 3 – "Linear Motion"
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Shembulli 3 - "Lëvizja lineare"
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Studioni tutorialin *Përdorni tastet e shigjetave* dhe krijoni një projekt ku macja drejtohet rreth skenës me tastierën.

|1| Shtoni bllokun |clicked_key| për macen.

|2| Zgjidhni tastin *Shigjeta e djathtë*.
 
|3| Zgjidhni |point_direction| bllokoni nga blloqet *Motion* dhe lidheni atë me bllokun e mëparshëm.

|4| Zgjidhni |move_steps| bllokoni nga blloqet *Motion* dhe lidheni atë me bllokun e mëparshëm.

|5| Shtypni tastin e djathtë të shigjetës në tastierën tuaj disa herë. Cfare ndodh?

|6| Kopjoni këtë skenar (kliko me të djathtën në bllokun e parë, më pas zgjidhni *Dublicate*).

|7| Në skenarin e ri, zëvendësoni shigjetën e djathtë me shigjetën e majtë, në pikën bllok *në drejtim* në vend të 90 zgjidhni -90.

|8| Shtypni tastin e majtë të shigjetës në tastierën tuaj disa herë. Cfare ndodh?

|9| Në mënyrë të ngjashme, bëni dy skenare të tjera: për të udhëhequr mace 10 hapa përpara duke shtypur tastin shigjetë lart, ose 10 hapa poshtë duke shtypur tastin poshtë shigjetës.
 
.. image:: ../_images/2/fig2_11.png
   :width: 480px   
   :align: center

.......

Shembulli 4 - "Lëvizja me një kthesë"
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Ne do të krijojmë një projekt më shumë për lëvizjen e sprites duke përdorur një tastierë, por me funksione të modifikuara të çelësave të shigjetave. Ne do t'i heqim blloqet për drejtimin dhe do të bashkohemi me butonin *shigjetë të majtë* dhe tastin *shigjetë të djathtë*me komandat të cilat rrotullohen sprite 15 gradë në të majtë ose në të djathtë. Gjithashtu, ne do të bashkohemi me tastin *shigjeta lart * dhe tastin *shigjetë poshtë* me bllokun ``lëvizni 10 hapa``,

.. image:: ../_images/2/fig2_12.png
   :width: 435px   
   :align: center

Ekzektuani projektin dhe provoni se si mund të menaxhoni lëvizjen e sprite.


|ask| E kuptuat?
-------------------------

Pyetja 1
~~~~~~~~~~

.. level:: 1

.. mchoice:: stage1
   :answer_a: 1280 pixels gjerë dhe 600 pixels gjatë
   :answer_b: 800 pixels gjerë dhe 600 pixels gjatë
   :answer_c: 480 pixels gjerë dhe 360 pixels gjatë
   :answer_d: 360 pixels gjerë dhe 480 pixels gjatë
   :correct: c
   :feedback_a: 
   :feedback_b: 
   :feedback_c: Saktë.
   :feedback_d: 
   
   Cilat janë dimensionet e Skenës?
   
Pyetja 2
~~~~~~~~~~

.. level:: 1

.. mchoice:: stage2
   :answer_a: në këndin e sipërm të majtë të Fazës
   :answer_b: në këndin e poshtëm të majtë të Fazës
   :answer_c: në qendër të Skenës
   :answer_d: varet nga sfondi i shtuar
   :correct: c
   :feedback_a: 
   :feedback_b: 
   :feedback_c: Saktë.
   :feedback_d: 
   
   Ku është vendndodhja e pikës me koordinatat (0,0)?
   
   
Pyetja 3
~~~~~~~~~~

.. level:: 1

.. mchoice:: blocks1
   :answer_a: Sensing 
   :answer_b: Motion
   :answer_c: Control
   :answer_d: Looks
   :correct: b
   :feedback_a: 
   :feedback_b: Saktë.
   :feedback_c: 
   :feedback_d: 
   
   Në cilin grup blloku i përket pozicioni, drejtimi, rotacioni dhe blloqet e menaxhimit të lëvizjes?
   

Pyetja 4
~~~~~~~~~~

.. level:: 1

.. mchoice:: stage3
   :answer_a: po
   :answer_b: jo
   :correct: b
   :feedback_a:  
   :feedback_b: Saktë.
   
    A mund të bllokojë Stage bllokimin e lëvizjes?

Pyetja 5
~~~~~~~~~~

.. level:: 2

.. mchoice:: absolute_motion
   :multiple_answers:
   :answer_a: 
   :answer_b: 
   :answer_c: 
   :answer_d: 
   :correct: a, d
   :feedback_a: 
   :feedback_b: 
   :feedback_c: 
   :feedback_d: 

   Cilët blloqe mundësojnë lëvizje absolute? (Zgjidhni të gjitha përgjigjet e sakta)

   .. image:: ../_images/2/q2_5.png
      :width: 530px   
      :align: center

Pyetja 6
~~~~~~~~~~

.. level:: 2

.. mchoice:: relative_motion
   :multiple_answers:
   :answer_a: 
   :answer_b: 
   :answer_c: 
   :answer_d: 
   :correct: b, d
   :feedback_a: 
   :feedback_b: 
   :feedback_c: 
   :feedback_d: 

   Cilët blloqe mundësojnë lëvizjen relative? (Zgjidhni të gjitha përgjigjet e sakta)

   .. image:: ../_images/2/q2_6.png
      :width: 530px   

Pyetja 7
~~~~~~~~~~

.. level:: 2

.. mchoice:: reporters
   :multiple_answers:
   :answer_a: 
   :answer_b: 
   :answer_c: 
   :answer_d: 
   :correct: b, c, d
   :feedback_a:  
   :feedback_b: 
   :feedback_c: 
   :feedback_d: 

    Cila nga blloqet përfaqëson reporterët në lëvizje? (Zgjidhni të gjitha përgjigjet e sakta)

   .. image:: ../_images/2/q2_7.png
      :width: 310px   
      :align: center


Pyetja 8
~~~~~~~~~~

.. level:: 3

.. image:: ../_images/2/q2_8.png
   :width: 400px   
   :align: center

.. mchoice:: compass
   :answer_a: Southeast
   :answer_b: Southwest
   :answer_c: Northeast
   :answer_d: Northwest
   :correct: d
   :feedback_a: Tregon kënd 135 gradë.
   :feedback_b: Tregon kënd -135 gradë.
   :feedback_c: Tregon kënd 45 gradë.
   :feedback_d: Saktë.
   
   Në cilën anë Sprite do ta shikojë pasi të drejtojë bllokun |2_8|?

.. |2_8| image:: ../_images/2/block2_8.png   

Pyetja 9
~~~~~~~~~~

.. level:: 1

Në figurën e mëposhtme mund të shihni një fazë me pesë pika të ndryshme.

.. image:: ../_images/2/q2_9.png
   :width: 300px   
   :align: center
      
.. mchoice:: coordinates1
   :answer_a: (-200,-40)
   :answer_b: (-200,40)
   :answer_c: (200,-40)
   :answer_d: (200,40)
   :correct: b
   :feedback_a:  
   :feedback_b: Saktë.
   :feedback_c: 
   :feedback_d: 
   
   Cilat janë koordinatat e Point A?
  
.. mchoice:: coordinates2
   :multiple_answers:
   :answer_a: Point A
   :answer_b: Point B
   :answer_c: Point D
   :answer_d: Point E
   :correct: b, d
   :feedback_a:  
   :feedback_b: 
   :feedback_c: 
   :feedback_d: 

   Cilat pikë kanë një koordinatë negative *y*?
    (Zgjidhni të gjitha përgjigjet e sakta)

.. dragndrop:: coordinates_various
   :feedback: Provo Përsëri
   :match_1: A|||(-200,40)
   :match_2: B|||(-160,-60)
   :match_3: C|||(20,0)
   :match_4: D|||(100,120)
   :match_5: E|||(180,-80)
    
   Duke tërhequr drejtkëndësat, çiftoni pikat me koordinatat e tyre.

Pyetja 10
~~~~~~~~~~~

.. level:: 2

Në figurën e mëposhtme mund të shihni një fazë me gjashtë pika të ndryshme.

.. image:: ../_images/2/q2_10.png
   :width: 300px   
   :align: center
      

.. dragndrop:: coordinates_symmetrical
    :feedback: Provo Përsëri
    :match_1: A|||(-160,80)
    :match_2: B|||(-160,-80)
    :match_3: C|||(160,-80)
    :match_4: D|||(80,0)
    :match_5: E|||(160,80)
    :match_6: F|||(0,80)
    
    Duke tërhequr drejtkëndësat, çiftoni pikat me koordinatat e tyre.

.. mchoice:: symmetry_х
   :answer_a: Point А
   :answer_b: Point В
   :answer_c: Point С
   :answer_d: Point D
   :correct: c
   :feedback_a: This should be the point which has the same x, and the opposite value of the y coordinate as the Point E. 
   :feedback_b: This should be the point which has the same x, and the opposite value of the y coordinate as the Point E.
   :feedback_c: Correct.
   :feedback_d: This should be the point which has the same x, and the opposite value of the y coordinate as the Point E.
   
   Which point is symmetrical to the Point E with respect to the *x* axis?

.. mchoice:: symmetry_у
   :answer_a: Point А
   :answer_b: Point В
   :answer_c: Point С
   :answer_d: Point D
   :correct: a
   :feedback_a: Saktë.
   :feedback_b: Kjo duhet të jetë pika që ka vlerën e kundërt të koordinatës x, dhe koordinatën e njëjtë y si Point E.
   :feedback_c: Kjo duhet të jetë pika që ka vlerën e kundërt të koordinatës x, dhe koordinatën e njëjtë y si Point E.
   :feedback_d: Kjo duhet të jetë pika që ka vlerën e kundërt të koordinatës x, dhe koordinatën e njëjtë y si Point E.
   
   Cilat pika janë ekuivalente nga boshti *y*? (Zgjidhni të gjitha përgjigjet e sakta)
 
.. mchoice:: symmetry2
   :multiple_answers:
   :answer_a: A dhe B
   :answer_b: A dhe C
   :answer_c: A dhe E
   :answer_d: D dhe F
   :correct: a, b, c
   :feedback_a: 
   :feedback_b: 
   :feedback_c: 
   :feedback_d: 

   Cilat pika janë ekuivalente nga boshti *y*? (Zgjidhni të gjitha përgjigjet e sakta)

|try| Provoje!
-------------

Ushtrimi 1 - Ndiq pozicionin e Sprite
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. level:: 1

.. infonote::

  |1| Tërhiqeni macen Sprite në këndin e sipërm të majtë të Stage, dhe pastaj kontrolloni informacionin Sprite për të parë koordinatat e pozicionit të ri.

  |2| Pastaj tërhiqeni atë në këndin e sipërm të djathtë të Stadit dhe kontrolloni përsëri koordinatat e pozicionit ku e keni lënë.

  |3| Përsëriteni atë që sapo keni bërë duke lëvizur Sprite-in tuaj në pjesën e poshtme të Fazës. Në cilat pozicione në Faza ka koordinata x vlera negative, dhe në cilin e bënë koordinatën y?

  |4| Importoni *Apple* Sprite nga libraria e Sprite. Një kornizë blu duhet të shfaqet rreth figurës së Sprite të re në listën Sprite, që do të thotë se Sprite është aktiv. Nëse jo, klikoni në figurën e saj në listën Sprite.
       
  |5| Kontrolloni variablat *х position* dhe *у position* në fund të grupit *Lëvizje* të blloqeve. Monitoruesit *Apple: x position* dhe *Apple: y position* do të shfaqen në Stage.

  |6| Tani tërhiqni *Apple* Sprite në pozicione të ndryshme në skenë dhe gjurmoni se si ndryshojnë koordinatat e tij duke shikuar monitorët.

.......

Ushrimi 2 - Vendosja e pozicionit të Sprite duke përdorur blloqet absolute të lëvizjes
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. level:: 2

.. infonote::

  |1| Klikoni në foton Stage pranë listës Sprite. Një kuti blu do të shfaqet rreth figurës së skenës, që do të thotë se Faza është në fokus.

  |2| Klikoni në ikonën *Zgjidhni një sfond* dhe më pas zgjidhni sfondin *Xy-grid* nga libraria *Backdrop*.

  |3| Tani klikoni në butonin *Code* për të marrë bllokun e paletës në vend të listës së sfondit.

  |4| Në blloqet *Motion* do të shihni një mesazh *Faza e zgjedhur: asnjë bllok lëvizjeje*, e cila është e kuptueshme sepse Skena, e cila tani është aktive, nuk mund të lëvizë.
  
  |5| Klikoni në pllakën e maceve në listën e sprite. Kur një kornizë blu shfaqet rreth figurës së sprite, blloqet *Motion* do të kthehen.

  |6| Zvarritni |goto_xy| bllokoni në zonën e shkrimeve, dhe pastaj ndryshoni vlerën e x në 120, dhe vlerën e y në 100.

  |7| Klikoni në bllokun e ndryshuar në zonën e shkrimeve. Cfarë ndodh?

  |8| Zvarritni |glide_xy| bllokoni në zonën e skriptit, dhe pastaj ndryshoni vlerën e x në -120, dhe vlerën e y në 100. Çfarë ndodh kur klikoni në këtë bllok?

  |9| Shikoni ku mund ta gjeni Sprite pasi të klikoni në bllokun në të cilin keni ndryshuar më parë vlerat për x dhe y. Për shembull, ku do të jetë Sprite nëse të dy koordinatat janë negative, nëse ato janë jashtë fazës, etj?

........

Ushtrimi 3 - Lëvizja relative dhe absolute
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. level:: 3

.. infonote::
   
  |Mundohuni të drejtoni Sprite nga pika A në pikën B duke përdorur blloqe të ndryshme *Lëvizjeje*.
   
  |1| Vendosni *Rrjetin* nga libraria e Sfondit si sfond.

  |2| Zgjidhni dy shkronja të reja nga libraria e sprite - shkronjat A dhe B (Blloku-A dhe Blloku-B).
  
  |3| Vendosni shkronjën A në këndin e poshtëm të majtë të Fazës në pozicionin (-200, -120), dhe shkronjën B në këndin e sipërm të djathtë në pozicionin (200, 120). Mënyra më e saktë për ta bërë këtë është të shtoni |goto_xy| bllokoni shkronjën A (tërhiqeni atë në zonën e shkrimeve ndërsa shkronja A është aktive) dhe shkruani koordinatat e duhura х dhe у, dhe pastaj klikoni në bllok. Ndiqni të njëjtat hapa për shkronjën B.
  
  |4| Shtoni bllokun |goto| për mace dhe zgjidhni *Block-A* nga lista drop-down (e cila do të shfaqet kur klikoni në trekëndëshin e bardhë në kutinë e zgjedhjes). **Shënim**. |Goto| |! = | |Goto_xy|.
   
  |5| Klikoni në bllokun |goto| dhe macja do të jetë pas shkronjës A.
  
  |6| Klikoni në blloku |goto_layer| nga grupi *Looks* blloqet dhe macja do të jetë përpara shkronjës A.
  
  .. image:: ../_images/2/ex2_3.png
     :width: 220px   
     :align: center

  |7| Tani në |goto| bllokoni zgjidhni *Block-B*, dhe pastaj klikoni mbi të. Macja do të jetë menjëherë përpara shkronjës B.

   |8| Shtoni bllokun |glide_to| për mace dhe zgjidhni *Block-A* nga lista drop-down, pastaj klikoni mbi të. Macja do të rrëshqasë për 1 sekondë te shkronja A. **Shënim**. |Glide_to| |! = | |Glide_xy|.
    
   |9| Provoni mënyrën e tretë. Së pari, shtoni | point_towards | bllok për mace, dhe nga lista drop-down zgjidhni opsionin ku macja tregon drejt sprite  Block-A*. **Shënim**. |Point_towards| |! = | |point_direction|

   Klikoni në |move_steps| bllokoni derisa macja të arrijë shkronjën A.

.......

Ushtrimi 4 - Përdorni bllokimin e stilit të rrotullimit dhe drejtimit
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. level:: 2

.. infonote::

 Krijoni një projekt në të cilin sprites do të sillet njësoj si sprites në projektin "Walk Dinosaur", por mos bëni ndonjë ndryshim në dritaren e informacionit Sprite. Në vend të kësaj, vendosni stilin e rrotullimit dhe drejtimin me skriptet e shtuara në sprites. Ruajeni këtë projekt nën emrin "Dinosaur Walk2".

.......

Ushtrimi 5 - Vendos Sprites te reja në projoekt 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

.. level:: 2

.. infonote::

Përdorni projektin "Ecni" për krijimin e një projekti të ri, ku do të prezantoni një spërkatje të re. Ky mund të jetë një qen ose një mi, i cili gjithmonë duhet të tregojë drejt mace. Shtoni sfondin e zgjedhjes suaj. Shtoni stilin e rrotullimit në skenarin që përcakton sjelljen e kësaj sprite të re. Mos bëni asnjë ndryshim në skenarin e shtuar në mace. Ruajeni këtë projekt nën emrin "Walk2".

|bug| Debug!
---------------

Bug 1
~~~~~~~~

Nxënësi dëshironte të bënte një animacion të thjeshtë të lëvizjes së maceve duke ndryshuar kostumin e tij. Prandaj, ai / ajo shtoi skenarin e mëposhtëm.

.. image:: ../_images/2/bug2_1.png
    :width: 220px 
    :align: center

Sidoqoftë, asgjë nuk ndodhi. Çfarë bëri gabim nxënësi?

Bug 2
~~~~~~~~

Nxënësi dëshironte që ura e tij të shkonte në mes të majtë dhe skajit të djathtë të Skenës. Kështu që ai / ajo futi kostumin *ndërprerës*, *lëvizin 10 hapa*, dhe bllokimet *në qoftë se kërcen* në bllokun e përsëritur përgjithmonë. Sidoqoftë, atij / asaj nuk i pëlqeu fakti që sprite po përballet në mënyrë të gabuar kur lëviz drejt skajit të majtë të skenës. Çfarë duhet të bëjë ai / ajo për të korrigjuar këtë?
   
  
|book| Përmbledhje
---------------------

Në këtë mësim, ne treguam se si mund të përcaktojmë pozicionin e saktë të një pike në skenë duke shikuar të dy koordinatat. Ne mund të dërgojmë sprita në një pozicion të veçantë në skenë duke përdorur blloqet lëvizëse absolute dhe relative. Lëvizja absolute është duke e zhvendosur Sprite në një lokacion të ri në skenë - destinacionin, pavarësisht nga pozicioni i saj i mëparshëm. Nga ana tjetër, lëvizja Relative është duke ndryshuar pozicionin e sprite në lidhje me pozicionin e saj të mëparshëm në skenë. Faza nuk mund të funksionojë blloqe lëvizjeje. Duke parë shembujt e projektit dhe duke bërë ushtrimet, mësuam se si mund të kontrollojmë lëvizjen e sprites tonë duke përdorur tastierën dhe miun tonë.

**Projekte Scratch**: 2Studio_

.. _2Studio: https://scratch.mit.edu/studios/25119440/

**Koncepte të reja**:  pixel, coordinate system, coordinates, motion blocks, motion reporters, absolute motion, relative motion, direction, rotation mode.

**Komanda Scratch**: |motion_blocks| - |move_steps|, |turn_right|, |turn_left|, |point_direction|, |point_towards|, |goto_xy|, |goto|,  |glide_xy|, |glide_to|, |set_x|, |set_y|, |change_x|, |change_y|, |if_edge|, |rotation_style|, |x_position|, |y_position|, |direction|; 

|events_blocks| - |clicked_key|; |looks_blocks| - |*| |goto_layer|,  |*| |switch_costume|; |control_blocks| - |*| |forever|.

Shënim. Blloqe të shënuara me |*| shenja do të diskutohet në mësimet që vijojnë.

|project| Krijoni projekte
---------------------------

Projekti 1 - "Dy lojtarë"
~~~~~~~~~~~~~~~~~~~~~~~~~~~

Filloni një projekt të ri që do ta quani "Dy Lojtaret". Vendos dy sprites në skenë, një në të majtë dhe tjetri në të djathtë. Vendosni sprites të tregojnë për njëri-tjetrin. Shtoni skriptet të cilat do t'i lejojnë ata të lëvizin përpara dhe mbrapa, dhe të kthehen në drejtim të akrepave të orës dhe të akrepave të sahatit.

Çelësat e kontrollit për Sprite-in e parë duhet të jenë:

• Up Arrow - Sprite shkon përpara në një vijë të drejtë,

• Arrow Down - Sprite kthehet në një vijë të drejtë,

• Shigjeta e majtë - Sprite kthehet në drejtim të akrepave të orës,

• Shigjeta e djathtë - Sprite kthehet në drejtim të akrepave të orës.

Çelësat e kontrollit për Sprite-in e dytë duhet të jenë:

• Key W - Sprite shkon përpara në një vijë të drejtë,

• Kyçi S - Sprite kthehet në një vijë të drejtë,

• Kyç A - Sprite kthehet në drejtim të akrepave të orës,

• Kyç D - Sprite kthehet në drejtim të akrepave të orës.
