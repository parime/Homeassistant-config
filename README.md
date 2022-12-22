Installation de [Home Assistant](https://home-assistant.io/) sous docker hébergé sur une VM debian 11, le tout sur un NAS Qnap. configuration pour un appartement T3, offrant des automatisations pour la lumière, le multimédia, la sécurité, etc...
Je ne suis pas un expert, les codes ne sont peut-être pas écrits de la meilleure façon, n'ayant à la base aucunes connaissances en développement et en Yaml, j'ai surtout modifié des configurations trouvées ici et là pour l'adapter à mon besoin, j'ai réalisé ceci avec mes petites connaissances et des informations trouvé un peu partout sur des sites, des forums et différents Github.


Tout n'est pas encore terminé, mais je commence à avoir quelques choses d'utilisable au quotidien, comme quoi même un novice avec un peu de patience et de persévérances peu arriver à avoir quelques choses de fonctionnel.


#### Lumières 💡

- **[Hue E27 White and Color Ambiance](https://www.philips-hue.com/fr-fr/p/hue-white-and-color-ambiance-pack-de-1-e27/8719514328204)** <sup>[Zigbee]</sup> salon (x3)
- **[Hue E27 White](https://www.philips-hue.com/fr-fr/p/hue-white-pack-de-1-e27/8719514329843)** <sup>[Zigbee]</sup> chambre 1 (x1), chambre 2 (x1), entrée (x1), WC (x1), cuisine (x1), hall (x1), Placard (x1)
- **[Hue Play](https://www.philips-hue.com/fr-fr/p/hue-white-and-color-ambiance-hue-play-pack-d-extension/7820330P7)** salon (x2).
- **[Ruban LED RGB 2m](https://fr.aliexpress.com/item/1005001629851565.html?spm=a2g0o.productlist.0.0.9a6641dcvSloLh&algo_pvid=11b74916-a0cf-4171-b561-42ae37cb1f9b&algo_exp_id=11b74916-a0cf-4171-b561-42ae37cb1f9b-7&pdp_ext_f=%7B%22sku_id%22%3A%2212000020734049678%22%7D&pdp_pi=-1%3B26.06%3B-1%3B-1%40salePrice%3BEUR%3Bsearch-mainSearch)** <sup>[Zigbee]</sup> cusine (x1)
- **[Ruban LED RGB 5m hue Lightstrips](https://www.amazon.fr/Philips-LightStrips-connectique-compatible-Bluetooth/dp/B088RX9CSZ/ref=sr_1_5?crid=17BYN0YNGI5AN&keywords=hue%2Blightstrip&qid=1671735585&sprefix=hue%2Bli%2Caps%2C91&sr=8-5&th=1)** hall (x1)
- **[Ruban LED RGB 5m étanche](https://fr.aliexpress.com/item/1005001629851565.html?spm=a2g0o.productlist.0.0.9a6641dcvSloLh&algo_pvid=11b74916-a0cf-4171-b561-42ae37cb1f9b&algo_exp_id=11b74916-a0cf-4171-b561-42ae37cb1f9b-7&pdp_ext_f=%7B%22sku_id%22%3A%2212000020734049678%22%7D&pdp_pi=-1%3B26.06%3B-1%3B-1%40salePrice%3BEUR%3Bsearch-mainSearch)** SdB (x1)

#### Noel 🎄🎅
- **[Twinkly Strings – Guirlande lumineuse à led](https://www.amazon.fr/gp/product/B08F2JDWX5/ref=ppx_yo_dt_b_asin_title_o09_s00?ie=UTF8&psc=1)** <sup>[Wifi]</sup>sapin salon (x1)
- **[Twinkly Music – Capteur de Son](https://www.amazon.fr/gp/product/B087CTR5VW/ref=ppx_yo_dt_b_asin_title_o08_s00?ie=UTF8&psc=1)** <sup>[Wifi]</sup> salon (x3)


#### Détécteurs 📡

- **[Xiaomi Aqara door & window contact sensor](https://www.amazon.fr/Aqara-XIAOMI-MCCGQ11LM-Ensemble-Capteur/dp/B07P9K6HBZ/ref=sr_1_5?crid=KW4W9BT65HNU&keywords=capteur+de+porte+xiaomi&qid=1644229999&sprefix=capteur+de+porte+xiaomi%2Caps%2C292&sr=8-5)** <sup>[Zigbee]</sup> détection d'ouverture de porte et fenêtres (x6). 
- **[Xiaomi MiJia human body movement sensor](https://www.amazon.fr/Aqara-RTCGQ11LM-D%C3%A9tecteur-Automatique-compatible/dp/B07D1CRRVF/ref=sr_1_6?__mk_fr_FR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=4A2UXBSNVBKD&keywords=capteur+de+mouvement+xiaomi&qid=1644147334&sprefix=capteur+de+mouvement+xiaomi%2Caps%2C51&sr=8-6)** <sup>[Zigbee]</sup> détection de mouvements (x9).
- **[Hue Détecteur de Mouvement Motion Sensor](https://www.amazon.fr/Philips-D%C3%A9tecteur-Mouvement-Motion-Sensor/dp/B09CV78GV1/ref=sr_1_5?__mk_fr_FR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=E0BNPR9KKMZM&keywords=hue+motion&qid=1644104262&sprefix=hue+motion%2Caps%2C54&sr=8-5)** <sup>[Zigbee]</sup> détection de mouvements (x3). 
- **[Xiaomi Aqara Capteur de Température et d'Humidité](https://www.amazon.fr/Aqara-Temperatur-Luftfeuchtigkeits-Luftdrucksensor-Homekit/dp/B07D37FKGY/ref=sr_1_6?crid=LMMOX7F8DMAO&keywords=aquara+xiaomi+temperature&qid=1644104335&sprefix=aquara+%2Caps%2C61&sr=8-6)** <sup>[Zigbee]</sup> Capteur de température et humidité (x8). 
- **[Xiaomi Capteur de luminosité](https://www.amazon.fr/Capteur-luminosit%C3%A9-Zigbee-3-0-Xiaomi/dp/B094MQC8V1/ref=sr_1_12?crid=OCWAI6ZJ4CHS&keywords=capteur+de+luminosit%C3%A9&qid=1644104676&sprefix=capteur+de+lu%2Caps%2C61&sr=8-12)** <sup>[Zigbee]</sup> Capteur de luminosité (x2). 
- **[Xiaomi Aqara Capteur de Vibration](https://www.amazon.fr/Capteur-vibration-sans-Aqara-DJT11LM/dp/B07PJT939B/ref=sr_1_20?__mk_fr_FR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=2ZK09VLWZS8IC&keywords=aqara+temperature+lcd&qid=1644104538&sprefix=aquara+temperature+lcd%2Caps%2C44&sr=8-20)** <sup>[Zigbee]</sup> Capteur de température et humidité (x2). 
- **[Xiaomi capteur de plante](https://www.amazon.fr/OLLIVAN-Intelligent-Bluetooth-Nutrition-Temp%C3%A9rature/dp/B01LXOJSWA/ref=sr_1_4?crid=1OA6N2B3HPMLW&keywords=capteur+plante+xiaomi&qid=1644104826&s=lawn-garden&sprefix=capteur+plante+xiao%2Cgarden%2C44&sr=1-4)** <sup>[Bluetooth]</sup> Capteur de température et humidité pour les plantes (x2).  **A venir!!**
- **[Détecteur de fumé](https://fr.aliexpress.com/item/4001360595304.html?spm=a2g0o.productlist.0.0.170e2932XINiPE&algo_pvid=14ebafa7-9d3a-4855-a8a8-201232dc337a&aem_p4p_detail=202202060336504889391504955280062854283&algo_exp_id=14ebafa7-9d3a-4855-a8a8-201232dc337a-44&pdp_ext_f=%7B%22sku_id%22%3A%2210000015799319920%22%7D&pdp_pi=-1%3B25.97%3B-1%3B-1%40salePrice%3BEUR%3Bsearch-mainSearch)** <sup>[Zigbee]</sup> Capteur de fumé (x1).

#### Media Players et autres appareils 📺

- **[PlayStation 4](https://www.amazon.fr/PS4-Slim-500-Go-noir/dp/B07HNR4ZZD/ref=sr_1_2?keywords=ps4&qid=1644104989&sr=8-2)** <sup>[ethernet]</sup> pour le contrôle local et vocal (on, off,...). **A venir!!**
- **[Nintendo switch](https://www.amazon.fr/Nintendo-Switch-avec-paire-Rouge/dp/B07WKNQ8JT/ref=sr_1_5?__mk_fr_FR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=2KVX793P5L1NQ&keywords=switch&qid=1644105032&sprefix=switch%2Caps%2C87&sr=8-5)** <sup>[Wifi]</sup> pour le contrôle local et vocal (on, off,...). **A venir!!**
- **[Plex](https://www.plex.tv/fr/)** <sup>[emulated]</sup> Pour la lecture de films et séries
- **[Alexa Echot Dot  (4e génération) avec horloge](https://www.amazon.fr/dp/B084J4KZ8J/ref=s9_acsd_al_bw_c2_x_2_i?pf_rd_m=A1X6FK5RDHNB96&pf_rd_s=merchandised-search-2&pf_rd_r=HP2Q3A3PY0QKZGX4FAH9&pf_rd_t=101&pf_rd_p=8df8ac55-eecf-4218-9fea-480a9c01e548&pf_rd_i=15428386031)** <sup>[WiFi]</sup> pour jouer de la musique dans les chambres et tout contrôler dans la maison (x3).
- **[Alexa Echo Dot (4e génération), Enceinte connectée avec Alexa, Anthracite](https://www.amazon.fr/dp/B084DWG2VQ/ref=pav_d_fromAsin_B07PHPXHQS_toAsin_B084DWG2VQ)** <sup>[WiFi]</sup> pour jouer de la musique dans le salon, la cuisine, la salle de bain et tout contrôler dans la maison (x3).

#### Prises 🔌

- **[Prises connectées](https://www.amazon.fr/dalimentation-intelligente-Application-t%C3%A9l%C3%A9commande-Fonctionne/dp/B09L4M7L8R/ref=sr_1_48?keywords=prise+zigbee&qid=1671736047&sr=8-48)** <sup>[ZigBee]</sup> pour contrôler et relever la consommation de mes appareils électroniques non inteligent(x5).
- **[Prises connectées avec USB et veilleuse](https://www.amazon.fr/Maxcio-Connect%C3%A9e-Intelligente-Compatible-Contr%C3%B4le/dp/B07GX8YDXZ)** <sup>[WiFi]</sup> pour contrôler et relever la consommation de mes appareils électroniques non inteligent(x2).

#### Télécommande et Bouton 🎛️

- **[Xiaomi Aqara wireless switch](https://www.amazon.fr/Aqara-Yiaomi-Filer-Mini-Schalter-Homekit/dp/B07D19YXND/ref=sr_1_2?__mk_fr_FR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=20S5C0EN646DQ&keywords=bouton+xiaomi&qid=1644103315&sprefix=bouton+xiaomi%2Caps%2C48&sr=8-2)** <sup>[Zigbee]</sup>  bouton sans fils (x4). 
- **[IKEA TRADFRI remote control](https://www.fibaro.com/fr/products/motion-sensor/)** <sup>[Zigbee]</sup> Télécommande pour allumer, éteindre, augmenter ou diminuer l’intensité lumineuse (x1). 
- **[HUE bouton intelligent](https://www.amazon.fr/Philips-t%C3%A9l%C3%A9commande-intelligent-connect%C3%A9-variateur/dp/B07SQZYYKL/ref=sr_1_5?__mk_fr_FR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=3SXYSCHRZAOR1&keywords=hue+bouton&qid=1644104030&sprefix=hue+bouton%2Caps%2C59&sr=8-5)** <sup>[Zigbee]</sup>  bouton sans fils (x1). 
- **[HUE Dim switch](https://www.amazon.fr/Philips-Switch-T%C3%A9l%C3%A9commande-variateur-lumi%C3%A8re/dp/B08PKMT2DV/ref=sr_1_6?__mk_fr_FR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=3SXYSCHRZAOR1&keywords=hue+bouton&qid=1644104095&sprefix=hue+bouton%2Caps%2C59&sr=8-6)** <sup>[Zigbee]</sup> Télécommande pour allumer, éteindre, augmenter ou diminuer l’intensité lumineuse (x1).
- **[HUE wall switch](https://www.amazon.fr/Philips-Lighting-929003017102-Module-dinterrupteur/dp/B09C62L43D/ref=sr_1_3?crid=T3NPS4IUCZLM&keywords=hue+wall+switch&qid=1644104141&sprefix=hue+wall%2Caps%2C53&sr=8-3)** <sup>[Zigbee]</sup> Domotiser des intérupteurs muraux standard (x10).

#### Camera et sirène 📽️

- **[Xiaomi 360- 1080p](https://www.amazon.fr/Xiaomi-Cam%C3%A9ra-s%C3%A9curit%C3%A9-connectivit%C3%A9-int%C3%A9rieur/dp/B08T99ZJGW/ref=sr_1_23?__mk_fr_FR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=3BWR89J9CSK9T&keywords=xiaomi+camera&qid=1644103542&sprefix=xiaomi+camera%2Caps%2C60&sr=8-23)** <sup>[WiFi]</sup> pour surveiller le chat et la maison en notre absence (x1).
- **[Sirene LSC Smart Connect](https://www.action.com/fr-fr/p/sirene-intelligente-lsc-smart-connect/)** <sup>[WiFi]</sup> Avertisseur sonore en cas d'intrusion dans la maison en notre absence (x1).

#### Aspirateur

- **[Xiaomi Roborock S6 MaxV ](https://www.amazon.fr/Roborock-aspirateur-Technologie-Reactiv-Superficie/dp/B08DHWLZSR/ref=sr_1_5?crid=3RZEVGCXWZPPW&keywords=roborock+s6+max+v&qid=1644106316&sprefix=roborock+s%2Caps%2C72&sr=8-5)** <sup>[WiFi]</sup> pour un nettoyage quotidien du sol (x1).

#### Hubs

- **[Hue Hub](https://www.amazon.fr/Philips-Hue-Pont-Connexion-Fonctionne/dp/B09CV9F3KR/ref=sr_1_5?__mk_fr_FR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=9IQ2ZU96JD83&keywords=hue+hub&qid=1644105522&sprefix=hue+hub%2Caps%2C58&sr=8-5)** <sup>[WiFi]</sup> pont de connexion pour l'ensemble des équipements HUE (x1).
- **[Combee II](https://www.amazon.fr/Dresden-ConBee-Electronique-II/dp/B07PZ7ZHG5/ref=sr_1_1?__mk_fr_FR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=3SJ6VTYF0X44E&keywords=conbee+2&qid=1644105724&sprefix=combee2%2Caps%2C64&sr=8-1)** <sup>[Zigbee]</sup> pont de connexion zigbee (x1). 

#### Mes intégrations

- **AdGuard Home**
- **local_ip**
- **Alarmo**
- **Alexa Media Player**
- **Application mobile**
- **Browser_mod**
- **CO2 signal**
- **Décodeur TV UHD**
- **myip**
- **Uptime**
- **Expiration du certificat**
- **File Size**
- **Google Cast**
- **HACS**
- **Supervisor**
- **Internet Printing Protocol (IPP)**
- **LocalTuya**
- **Moon**
- **Home**
- **MyEnedis**
- **Météo-France**
- **Philips hue**
- **Profiler**
- **SpeedTest**
- **Radio browser**
- **Season**
- **Sun**
- **Spotify**
- **UPnP/IGD**
- **Version**
- **Xiaomi Miio**
- **Xiaomi Miot Auto**
- **ZHA**

#### TO DO projets 

- **Serre connectée** Création d'une serre <sup>[Diy, nok]</sup> pour les Orchidées de madame avec contrôle de température et hygromètrie **[Xiaomi capteur de plante](https://www.amazon.fr/OLLIVAN-Intelligent-Bluetooth-Nutrition-Temp%C3%A9rature/dp/B01LXOJSWA/ref=sr_1_4?crid=1OA6N2B3HPMLW&keywords=capteur+plante+xiaomi&qid=1644104826&s=lawn-garden&sprefix=capteur+plante+xiao%2Cgarden%2C44&sr=1-4)** <sup>[Bluetooth]</sup>, éclairage via bandeau LED - **[Ruban LED RGB 5m étanche](https://fr.aliexpress.com/item/1005001629851565.html?spm=a2g0o.productlist.0.0.9a6641dcvSloLh&algo_pvid=11b74916-a0cf-4171-b561-42ae37cb1f9b&algo_exp_id=11b74916-a0cf-4171-b561-42ae37cb1f9b-7&pdp_ext_f=%7B%22sku_id%22%3A%2212000020734049678%22%7D&pdp_pi=-1%3B26.06%3B-1%3B-1%40salePrice%3BEUR%3Bsearch-mainSearch)** (x1) <sup>[Zigbee]</sup>, arrosage [Système d'arrosage intelligent Tuya](https://www.amazon.fr/OLLIVAN-Intelligent-Bluetooth-Nutrition-Temp%C3%A9rature/dp/B01LXOJSWA/ref=sr_1_4?crid=1OA6N2B3HPMLW&keywords=capteur+plante+xiaomi&qid=1644104826&s=lawn-garden&sprefix=capteur+plante+xiao%2Cgarden%2C44&sr=1-4) <sup>[Bluetooth,zigbee]</sup>, niveau du réservoir d'eau **A venir!!**

- **Bac de culture extérieur** Création bac de culture <sup>[Diy, ok]</sup> pour réaliser un petit potagé sur le balcon avec contrôle de température et hygromètrie **[Xiaomi capteur de plante](https://www.amazon.fr/OLLIVAN-Intelligent-Bluetooth-Nutrition-Temp%C3%A9rature/dp/B01LXOJSWA/ref=sr_1_4?crid=1OA6N2B3HPMLW&keywords=capteur+plante+xiaomi&qid=1644104826&s=lawn-garden&sprefix=capteur+plante+xiao%2Cgarden%2C44&sr=1-4)** <sup>[Bluetooth]</sup> arrosage [Système d'arrosage intelligent Tuya](https://www.amazon.fr/OLLIVAN-Intelligent-Bluetooth-Nutrition-Temp%C3%A9rature/dp/B01LXOJSWA/ref=sr_1_4?crid=1OA6N2B3HPMLW&keywords=capteur+plante+xiaomi&qid=1644104826&s=lawn-garden&sprefix=capteur+plante+xiao%2Cgarden%2C44&sr=1-4) <sup>[Bluetooth,zigbee]</sup>, niveau du réservoir d'eau **A venir!!**

- **Miroir magic** Création d'un miroir magic <sup>[Diy]</sup> **A venir!!**

- **[Lave linges et lave vaisselles]** Contrôle de fonctionnement et état du cycle via [**[Prises connectées](https://www.amazon.fr/Connect%C3%A9e-intelligente-compatible-SmartThings-Surveillance/dp/B08ZY72GS6/ref=sr_1_21?crid=HKBNDJ0M7HU0&keywords=prise+connecter+alexa&qid=1644103013&s=hi&sprefix=prise+connecter%2Cdiy%2C52&sr=1-21)** <sup>[WiFi]</sup> et **[Xiaomi Aqara Capteur de Vibration](https://www.amazon.fr/Capteur-vibration-sans-Aqara-DJT11LM/dp/B07PJT939B/ref=sr_1_20?__mk_fr_FR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=2ZK09VLWZS8IC&keywords=aqara+temperature+lcd&qid=1644104538&sprefix=aquara+temperature+lcd%2Caps%2C44&sr=8-20)** <sup>[Zigbee]</sup>. **A venir!!**

- **[PlayStation 4](https://www.amazon.fr/PS4-Slim-500-Go-noir/dp/B07HNR4ZZD/ref=sr_1_2?keywords=ps4&qid=1644104989&sr=8-2)** <sup>[ethernet]</sup> pour le contrôle local et vocal (on, off,...). **A venir!!**

- **[Nintendo switch](https://www.amazon.fr/Nintendo-Switch-avec-paire-Rouge/dp/B07WKNQ8JT/ref=sr_1_5?__mk_fr_FR=%C3%85M%C3%85%C5%BD%C3%95%C3%91&crid=2KVX793P5L1NQ&keywords=switch&qid=1644105032&sprefix=switch%2Caps%2C87&sr=8-5)** <sup>[Wifi]</sup> pour le contrôle local et vocal (on, off,...). **A venir!!**

- **Boite aux lettres** <sup>[Zigbee]</sup> pour le contrôle du courrier et des colis. **A venir!!**


#### <a name="screenshots thème clair">Screenshots thème clair</a>

<div align="center">
    <figure>
        <div>
            <img src="/www/images/Dshboard_ligth_home_1.PNG" title="Vues">
        </div>
        <figcaption>
            <p><strong> </strong></p>
        </figcaption>
    </figure>
    </div>

<div align="center">
    <figure>
        <div>
            <img src="/www/images/Dshboard_ligth_home_2.PNG" title="Vues">
        </div>
        <figcaption>
            <p><strong>Vue global</strong></p>
        </figcaption>
    </figure>
    </div>
    
<div align="center">
    <figure>
        <div>
            <img src="/www/images/Dshboard_ligth_meteo_1.PNG" title="Vues">
        </div>
        <figcaption>
            <p><strong> </strong></p>
        </figcaption>
    </figure>
    </div>
		
<div align="center">
    <figure>
        <div>
            <img src="/www/images/Dshboard_ligth_meteo_2.PNG" title="Vues">
        </div>
        <figcaption>
            <p><strong>Onglet météo, température et humidité des pièces</strong></p>
        </figcaption>
    </figure>
    </div>
    
<div align="center">
    <figure>
        <div>
            <img src="/www/images/Dshboard_ligth_fllorplan_1.PNG" title="Vues">
        </div>
        <figcaption>
            <p><strong> </strong></p>
        </figcaption>
    </figure>
    </div>
    
<div align="center">
    <figure>
        <div>
            <img src="/www/images/Dshboard_ligth_fllorplan_2.PNG" title="Vues">
        </div>
        <figcaption>
            <p><strong>Onglet Floorplan</strong></p>
        </figcaption>
    </figure>
    </div>
    
<div align="center">
    <figure>
        <div>
            <img src="/www/images/Dshboard_ligth_information_1.PNG" title="Vues">
        </div>
        <figcaption>
            <p><strong>Onglet information</strong></p>
        </figcaption>
    </figure>
    </div>

<div align="center">
    <figure>
        <div>
            <img src="/www/images/Dshboard_ligth_server_1.PNG" title="Vues">
        </div>
        <figcaption>
            <p><strong>Onglet supervision</strong></p>
        </figcaption>
    </figure>
    </div>

<div align="center">
    <figure>
        <div>
            <img src="/www/images/Dshboard_ligth_automation_1.PNG" title="Vues">
        </div>
        <figcaption>
            <p><strong>Onglet automatisations, scripts, scènes, éclairage</strong></p>
        </figcaption>
    </figure>
    </div>

<div align="center">
    <figure>
        <div>
            <img src="/www/images/Dshboard_ligth_module_1.PNG" title="Vues">
        </div>
        <figcaption>
            <p><strong>HACS Intégrations</strong></p>
        </figcaption>
    </figure>
    </div>
	
<div align="center">
    <figure>
        <div>
            <img src="/www/images/Dshboard_ligth_module_1.PNG" title="Vues">
        </div>
        <figcaption>
            <p><strong>HACS Interface</strong></p>
        </figcaption>
    </figure>
    </div>

#### Mes sources


- **[HACF](https://forum.hacf.fr/)**  <sup>[fr]</sup>  Forum francophone sur home-assistant.
- **Journal de Thomas** [Chaine youtube](https://www.youtube.com/c/JournaldeThomas/playlists)<sup>[fr]</sup> et [Github](https://github.com/journaldethomas/home-assistant-config)<sup>[fr]</sup>
- **Paradis Artificiels** [Chaine youtube](https://www.youtube.com/channel/UCbCJtFizTFNf4waPWPFAqcA)<sup>[fr]</sup> et [Github](https://github.com/romquenin/home-assistant-config-fr)<sup>[fr]</sup>
- **Herve AUREL** [Github](https://github.com/herveaurel/HomeAssistant)<sup>[fr]</sup>
- **Oncleben31** [Github](https://github.com/oncleben31/home-assistant-config)<sup>[fr-en]</sup>
- **Franck Nijhof-Frenck** [Github](https://github.com/frenck/home-assistant-config)<sup>[en]</sup>
- **[Groupe Facebook](https://www.facebook.com/groups/homeassistantgroupefranceGroupe)**<sup>[fr]</sup>
