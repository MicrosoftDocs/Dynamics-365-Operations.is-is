---
title: "Skipuleggja fyrirtækjastigveldi"
description: "Áður en að setja upp fyrirtæki og stigveldi fyrirtækis skaltu ganga úr skugga um að þú skiljir hvernig best er að setja upp fyrirtækið."
author: sericks007
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: OMHierarchyManager, OMLegalEntity, OMOperatingUnit
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 17404
ms.assetid: babde0c6-bb5d-45ae-95ca-2af75a0ea292
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d669defa13e8f32cd29463324e580a6d738c3e2a
ms.contentlocale: is-is
ms.lasthandoff: 11/03/2017

---

# <a name="plan-your-organizational-hierarchy"></a>Skipuleggja fyrirtækjastigveldi

[!include[banner](../includes/banner.md)]


Áður en þú setur upp fyrirtæki og stigveldi fyrirtækis í Microsoft Dynamics 365 for Finance and Operations skaltu áætla hvernig fyrirtækjalíkanið þitt verður. Fyrirtækjalíkan hefur töluverð áhrif á innleiðingu á Finance and Operations og í viðskiptaferlum. 

Stigveldi fyrirtækis standa fyrir vensl á milli fyrirtækja sem eru saman í rekstri. Þess vegna er mikilvægasta tillit þegar þú líkans fyrirtæki skipulag fyrirtækisins. Mælt er með því að skilgreina skipulag fyrirtækis sem er byggð á svörun frá executives og aðalbókara stjórnendur úr virkum svæðum, s.s. fjármál og bókhaldi, mannauður, aðgerðir, innkaup og sala og markaðsstarf. 

Þegar þú skipuleggur stigveldi er einnig mikilvægt að huga að tengslum milli stigveldiskipulags og fjárhagsvídda. Þú getur sett upp mörg fyrirtækisstigveldi til að birta mismunandi ásýndir fyrirtækis þíns. Með því að nota fjárhagsvíddir er hægt að stofna skýrslur byggðar á þessum yfirlitum. Stofnaðu, í samvinnu við Dynamics 365 for Finance and Operations samstarfsaðilannn, stigveldi sem lýtur að skýrslugjöf, lögbundinni og innan fyrirtækisins. 

> [!Note]
> Þó að þú getir notað fjárhagsvíddir til að tákna lögaðila án þess að stofna lögaðila í Finance and Operations, eru fjárhagsvíddir ekki hannaðar til að takast á við reksturs- eða viðskiptaþarfir lögaðila. Eiginlekin millieiningabókhalds í Finance and Operations er hannaður til að eiga aðeins við bókhaldsfærslur sem eru stofnaðar fyrir hverja færslu. 

> [!Caution]
> Ekki ætti að ákveða hvernig skal móta fyrirtæki þitt byggt eingöngu á upplýsingunum í þessari grein. Þessi fylgigögn eru leiðbeiningar. Hafðu samráð við Finance and Operations samstarfsaðilann til að fá frekari leiðbeiningar. Finance and Operations samstarfsaðilinn hefur reynslu innan ýmissa atvinnugreina og af samstarfi við alls konar viðskiptavini.

## <a name="decide-whether-to-model-internal-organizations-as-legal-entities-or-operating-units"></a>Ákveða hvort líkanið samstæðufyrirtæki sem lögaðilum eða rekstrareiningum

Það verður minnst einn lögaðili að vera fulltrúi fyrirtækisins í Finance and Operations. Lögaðili getur fært inn lögbundna samninga og ætlast er til að það búi til fjárhagsskýrslur sem veita skýrslur um afköst hans. 

Í Finance and Operations er hægt að nota lögaðila fyrir viðskiptaferli eða sameiningu. Þetta þýðir að lögaðili í Finance and Operations stendur ekki endilega fyrir raunverulegan aðila í fyrirtækinu. Fyrirtækið sem tekur þátt í færslur geta til dæmis átt dótturfyrirtæki lögaðila. Í þessari atburðarás er lögaðili nauðsynlegur fyrir færslur og sýndarlögaðila þarf til að sameina niðurstöður og stöður undirlögaðila. 

Innri stofnanir í fyrirtæki þitt, svo sem svæðisskrifstofur, má kynna sem fleiri lögaðila eða rekstrareiningar hjá helsta lögaðila. Ekki er krafist að rekstrareining sé löglega skilgreind stofnun. Rekstrareiningar eru notuð til að stjórna efnahag og aðgerðum aðferð í bransanum. Til dæmis, deildir og kostnaðarstaði eru rekstrareiningar. 

Sum virkni í Finance and Operations virkar mismunandi eftir því hvort fyrirtæki er lögaðili eða rekstrareining. Íhugaðu vandlega virknina sem lýst er hér að neðan þegar þú tekur ákvörðun þína. 


### <a name="master-data"></a>Aðalgögn
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ef fyrirtækið er með líkan sem lögaðili      
Sumir aðalgögn, svo sem viðskiptavinir, greiðsluskilmálar, skattyfirvöld og staðbundna birgðaröðun, skal setja upp fyrir hvern lögaðila. Sumir aðalgögn, svo sem notendur, vörur og flest mannauðsgögn, er deilt með öllum lögaðilum. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ef fyrirtækið er með líkan sem rekstrareining 
Aðalgögnum er deilt meðal rekstrareiningar. 

### <a name="module-parameters"></a>Færibreytur kerfis
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ef fyrirtækið er með líkan sem lögaðili    
Færibreytur fyrir kerfiseiningar, eins og Færibreytur viðskiptakrafa, Færibreytur viðskiptaskulda og Færibreytur reiðufjár- og bankastjórnunar, verða að vera stilltar fyrir hvern lögaðila. Þar sem uppsetningu leiðarkerfis lögaðila er aðskildar hvers dótturfyrirtækis getur samræmast staðbundna lögboðnu þarfir og venjur viðskiptatengsl. Til dæmis getur lögaðili með sérfræðiþjónustu og framleiðslulögaðili haft mismunandi færibreytur kerfishluta jafnvel þótt þeir tilheyri sama móðurfyrirtækinu. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ef fyrirtækið er með líkan sem rekstrareining 
Færibreytum kerfis eru deilt á milli rekstrareininga. 

### <a name="data-security"></a>Öryggi gagna
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ef fyrirtækið er með líkan sem lögaðili    
Flest gögn er sjálfkrafa tryggð með fyrirtækjakenni. Kenni fyrirtækis er einkvæmt kenni fyrir gögnin sem tengjast lögaðilanum. Fyrirtæki er aðeins hægt að tengja við einn lögaðila og lögaðila er aðeins hægt að tengja við eitt fyrirtæki. Notendur geta nálgast gögn aðeins fyrir þau fyrirtæki sem þeir hafa aðgang að. Ekki þarf að sérsníða Finance and Operations til að tryggja gögn með auðkenni fyrirtækis. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ef fyrirtækið er með líkan sem rekstrareining 
Öryggisvörðum getur eftir rekstrareiningu gögn með því að stofna öryggisreglur sérsniðnum gögnum. Öryggisreglur gagna eru notaðar til að takmarka aðgang að gögnum. Til dæmis, gefum okkur að notanda sé heimilt að stofna innkaupapantanir einungis í tiltekinn rekstrareiningu. Hægt er að stofna öryggisreglur gagna til að koma í veg fyrir að notandinn hafi aðgang að gögnum innkaupapöntun úr annarri rekstrareiningu. Rúmmál færslna og fjölda öryggisreglur geta haft áhrif á afköst. Þegar öryggisreglur eru hannaðar, skal hafa afköst í huga. 

### <a name="ledgers"></a>Fjárhagur
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ef fyrirtækið er með líkan sem lögaðili    
Hver lögaðila krefst fjárhags sem veitir bókhaldslykils lykla bókhaldsgjaldmiðill, skýrslugjaldmiðill og fjárhagsdagatal. Hægt er að stofna efnahagsreikningur aðeins fyrir lögaðila. Aðallyklar, víddir, lykilskipulag, bókhaldslyklar og reikningsreglur má nota af fleirum en einum lögaðila.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ef fyrirtækið er með líkan sem rekstrareining 
Rekstrareining getur ekki haft eigin fjárhagsupplýsingar. Ef notanda samstæðufyrirtæki þurfa ekki einkvæmt fjárhag, hægt að móta þær sem rekstrareiningar. Fjárhagsupplýsingar verða settar upp fyrir yfireiningu lögaðila í stigveldi. Rekstrarreikninga má búa til fyrir rekstrareiningar innan lögaðila eða fyrir yfireiningar lögaðila. 

### <a name="fiscal-calendars"></a>Fjárhagsdagatöl 
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ef fyrirtækið er með líkan sem lögaðili    
Hver lögaðili er með eigið fjárhagsdagatal. Ef samstæðufyrirtæki þitt nota mismunandi fjárhagsár og fjárhagsdagatal, verður að móta fyrirtæki sem lögaðila. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ef fyrirtækið er með líkan sem rekstrareining 
Rekstrareiningar verða að deila fjárhagsdagatali. Ef samstæðufyrirtæki þitt getur deila sama fjárhagsár og fjárhagsdagatal, er hægt að móta fyrirtæki sem rekstrareiningar. 

### <a name="consolidation"></a>Samstæða
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ef fyrirtækið er með líkan sem lögaðili    
Sameina verður fjárhagsniðurstöður svæðisbundið skrifstofur í eina, sameinað fyrirtæki til að útbúa fjárhagsskýrslur. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ef fyrirtækið er með líkan sem rekstrareining 
Sameining er ekki krafist, þar sem gögn eru þegar samnýtt milli rekstrareininga. 

### <a name="centralized-payments"></a>Miðstýrðar greiðslur
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ef fyrirtækið er með líkan sem lögaðili 
Miðstýrðar greiðslur verður að setja upp þannig að hægt er að greiða reikninga fyrir alla lögaðila undirstig til eða frá einni yfirlögaðila. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ef fyrirtækið er með líkan sem rekstrareining 
Miðstýrðar greiðslur er krafist vegna þess að allir reikningar eru skráðar í einni lögaðila.

### <a name="intercompany-transactions"></a>Færslur innan samstæðu
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ef fyrirtækið er með líkan sem lögaðili 
Samstæðusölupöntun, innkaupapantanir, greiðslur eða kvittanir er hægt að jafna saman. Ekki er þörf á að nota fylgiskjöl færslubóka. Hægt er að skoða samstæðufærslur stigi undirfjárhag (Viðskiptakröfur, Viðskiptaskuldir). Eftirfarandi dæmi sýna hvernig færslur eru meðhöndlaðar. 

##### <a name="example-1-headquarters-provides-services-to-regional-offices-and-must-charge-the-costs-of-those-services-to-the-regional-offices"></a>Dæmi 1:. Höfuðstöðvar veitir þjónustu til svæðisskrifstofa og verðum að rukka kostnað af þessari þjónustu til svæðisskrifstofa
Ef þú mótar svæðisskrifstofuna sem lögaðila hefurðu eftirfarandi valkosti: 
- Höfuðstöðvar skapa dagbókarfærslu til rukka svæðisráð um kostnað. Ekki er hægt að aldursgreina færslur.
- Höfuðstöðvar sendir innkaupapöntun fyrir þjónustu til svæðisráðum. Sölupöntun er stofnuð sjálfkrafa í reitnum lögaðili fyrir svæðisbundið skrifstofu, með undirfjárhagsfærslu innan samstæðu. 

##### <a name="example-2-headquarters-procures-and-pays-for-service-that-is-delivered-to-a-regional-office"></a>Höfuðstöðvar kaupir og greiðir fyrir þjónustu sem er skilað til svæðisskrifstofu
Ef þú mótar svæðisskrifstofuna sem lögaðila hefurðu eftirfarandi valkosti: 
- Reikningar og greiðslur fylgja reglum höfuðstöðvar. Höfuðstöðvar geta stofnað færslu á milli fyrirtækja til að innheimta fyrir kostnaði þvert á svæðisbundnar skrifstofur. Ekki er hægt að aldursgreina færslur. 
- Reikningar og greiðslur fylgja reglum höfuðstöðvar. Höfuðstöðvar geta stofnaða færslu fyrir undirfjárhag þvert á skrifstofur.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ef fyrirtækið er með líkan sem rekstrareining 
Samstæðufærslur meðal rekstrareininga eru aðeins studdar gegnum færslubókarfylgiskjöl. Rekstrareining getur ekki gefið út eða móttekið innkaupapöntun, sölupöntun eða reikning úr annarri rekstrareiningu sama lögaðila. Hægt er að skoða samstæðufærslur stigi undirfjárhag (Viðskiptakröfur, Viðskiptaskuldir). Eftirfarandi dæmi sýna hvernig færslur eru meðhöndlaðar. 

##### <a name="example-1-headquarters-provides-services-to-regional-offices-and-must-charge-the-costs-of-those-services-to-the-regional-offices"></a>Dæmi 1:. Höfuðstöðvar veitir þjónustu til svæðisskrifstofa og verðum að rukka kostnað af þessari þjónustu til svæðisskrifstofa
Ef þú setur svæðisskrifstofuna upp sem rekstrareiningu, færa höfuðstöðvar inn kostnaðarfærslu og kóðar það sem svæðisskrifstofu. 

##### <a name="example-2-headquarters-procures-and-pays-for-service-that-is-delivered-to-a-regional-office"></a>Dæmi 2:. Höfuðstöðvar kaupir og greiðir fyrir þjónustu sem er skilað til svæðisskrifstofu
Ef þú setur svæðisskrifstofuna upp sem rekstrareining, fara reikningar og greiðslur eftir kröfum sem koma fram í reglum höfuðstöðva. Reikningur hægt kóðaðir til svæðisbundið skrifstofu. Á rekstrarreikningi nota afstemmingarfjárhagsvídd að tilkynna kostnað fyrir svæðisskrifstofu.

### <a name="local-tax-requirements"></a>Staðbundnar skattakröfur
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ef fyrirtækið er með líkan sem lögaðili
Lögaðili fellur undir lög um skatt af skattayfirvöldum í landi/svæði þar sem lögaðili er skráð. Til dæmis fellur lögaðili sem er skráður í Danmörku undir dönsk skattalög og -reglur. Í Finance and Operations getur lögaðili aðeins tilheyrt einu landi/svæði. Landið/svæðið sem valið er fyrir aðalaðsetur lögaðilans stýrir lands/svæðisbundnum aðgerðum sem eru tiltækar fyrir lögaðilann. Til dæmis, ef aðalaðsetur lögaðilans er í Danmörku verða aðgerðir sem tengjast dönskum skattalögum og -reglugerðum tiltækar. Þess vegna ef fyrirtæki þitt eru í öðrum löndum/svæðum og krefjast mismunandi staðbundna skattavalkosti, setja verður upp fyrirtæki sem aðskilda lögaðila.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ef fyrirtækið er með líkan sem rekstrareining 
Rekstrareiningar nota landssamhengi yfirlögaðila. Rekstrareiningar í sama lögaðila geta ekki haft mismunandi lands-/svæðistilgreindar kröfur. Ef fyrirtæki þitt eru í sama landi/svæði og nota sömu skattavalkosti er hægt að setja þá upp sem rekstrareiningar.


### <a name="statutory-reporting-for-a-countryregion"></a>Lögbundinn skýrsla fyrir land / svæði 
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ef fyrirtækið er með líkan sem lögaðili
Hægt er að stofna flestar lögboðnar skýrslur fyrir lönd/svæði sem eru studd í Finance and Operations. Sjá upplýsingar um hvaða skýrslur eru tiltækar fyrir hvert land/svæði í [Microsoft Dynamics Staðfærslugátt](https://mbs.microsoft.com/customersource/global/ax/support/support-news/GFMLocalizationPortalMC) fyrir Finance and Operations. (CustomerSource innskráningar er krafist.) 

> [!Note]
> Í Finance and Operations gerir bókunarlag kleift að gera leiðréttingarfærslur á móðurfyrirtæki sem notar annan bókhaldsstaðal en dótturfyrirtæki. Til dæmis, fyrir fyrirtæki sem notar almennt samþykkt bókhaldsvenjum í Bretland (UK GAAP), er hægt að gera leiðréttingarfærslur í bókunarlag. Hægt er að sameina þessar færslur inn móðurfyrirtækis sem samþykkt notar almennt reikningsskilareglur (samþykktum Bókhaldsreglum) í Bandaríkjunum. Leiðréttingarfærslur sem hafa ekki áhrif á samþykktum Bókhaldsreglum UK skýrslugerð.

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ef fyrirtækið er með líkan sem rekstrareining 
Lögbundinn skýrslur verður að stofna með annað forrit. Það þarf að tryggja að gögnin séu sótt í Finance and Operations til að styðja þarfir hverrar rekstrareiningar, þar sem þær eru frábrugðnar kröfum höfuðstöðva. 

### <a name="currency"></a>Gjaldmiðill
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ef fyrirtækið er með líkan sem lögaðili
Ef fyrirtæki þitt verður að nota mismunandi virka gjaldmiðla, þarf að móta fyrirtæki sem lögaðila. Virkir gjaldmiðlar eru settir upp fyrir hvern lögaðila. Hins vegar er hægt að færa inn færslur í mörgum gjaldmiðlum. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ef fyrirtækið er með líkan sem rekstrareining 
Ef fyrirtæki þitt getur notað einn virkan gjaldmiðli, má móta fyrirtæki sem rekstrareiningar. Rekstrareiningar verða að deila starfrækslugjaldmiðli. Hins vegar hægt að færa inn færslur og stofnað skýrslur í mörgum gjaldmiðlum. 


### <a name="year-end-closing"></a>Lokun í árslok
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ef fyrirtækið er með líkan sem lögaðili
Ef lögum og bókhaldsreglum eru mismunandi á milli löndum/svæðum þar sem fyrirtæki þitt er, gæti krafist mismunandi ársloka ferli fyrir hvert fyrirtæki. Þetta þýðir að þarf líkanið fyrirtæki sem lögaðila. Hver lögaðila hefur sín eigin árslokaferli. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ef fyrirtækið er með líkan sem rekstrareining 
Lögum og bókhaldsreglum eru sömu milli löndum/svæðum þar sem fyrirtæki þitt er hægt að nota eitt safn ársloka ferli. Þetta þýðir að hægt model fyrirtæki sem rekstrareiningar. Allir rekstrareiningar verða að nota sama ferli fyrir lökun í árslok. 
   
### <a name="number-sequences"></a>Númeraraðir
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ef fyrirtækið er með líkan sem lögaðili
Hægt er að setja upp númeraraðir fyrir nokkrar tilvísanir á hvern lögaðila. Sumir númeraraðir hægt að deila. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ef fyrirtækið er með líkan sem rekstrareining 
Hægt er að setja upp númeraraðir fyrir nokkrar tilvísanir á hverja rekstrareiningu. Sumir númeraraðir hægt að deila.

### <a name="products"></a>Afurðir 
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ef fyrirtækið er með líkan sem lögaðili
Afurðarskilgreiningar eru samnýttar og þær verður að losa til einstaka lögaðila áður en hægt er að hafa þeir í færslum. Hver lögaðila hefur sína eigin útgefnar afurðir sem hægt er að taka með í skjölum á færslu. Ef samstæðufyrirtæki þitt verður að nota mismunandi hóp afurða, er verður að móta fyrirtæki sem lögaðila. 

> [!Note]
> Jafnvel þótt afurðarskilgreiningar eru samnýttar hjá öllum lögaðilum þar sem afurð hefur verið losað, er hægt að tilgreina mismunandi sölu, innkaupa- og geyma færibreytur fyrir vöruna á hverja birgðasvæði. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ef fyrirtækið er með líkan sem rekstrareining 
Allar rekstrareiningar deila sama mengi af afurðum. Ef samstæðufyrirtæki þitt getur deila sama hóp afurða, er hægt að móta fyrirtæki sem rekstrareiningar. 

### <a name="inquiry-and-reporting"></a>Fyrirspurn og skýrslugerð  
#### <a name="if-the-organization-is-modeled-as-a-legal-entity"></a>Ef fyrirtækið er með líkan sem lögaðili
Handvirkt breyta verður fyrirtæki til að færa inn færslur og gera fyrirspurnir í marga lögaðila. Vegna marka öryggi gagna, sameinaða fyrirspurnina og skýrslugerð getur verið tímafrekt og viðtökueininga tilfangs. 

#### <a name="if-the-organization-is-modeled-as-an-operating-unit"></a>Ef fyrirtækið er með líkan sem rekstrareining 
Ekki þarf að breyta fyrirtæki til að nálgast gögn frá mörgum rekstrareiningar. Fyrirspurn um sameinaða og skýrslugerð og einstaka svæðisbundið fyrirspurn er auðveldara og hraðar.

## <a name="best-practices-for-modeling-organizations-and-hierarchies"></a>Bestu venjur fyrir líkanabreytur fyrirtæki og stigveldi
Íhugið eftirfarandi bestu venjur þegar komið stigveldi fyrirtækis:
-   Stofna deild sem líkanið intersection milli lögaðila og einingu viðskiptatengsl. Þú getur þá tekið saman gögn frá deild til lögaðila fyrir lögbundin skýrslugerð, og frá deild til viðskiptaeiningu fyrir innri skýrslugjöf. Deildir geta þjónað sem hagnaðarstað. Ef deildir eru notaðar, þarf ekki að nota lögaðila og viðskiptaeiningar sem víddir í lykilskipulagi. Hægt er að nota bara deildir sem sem vídd. Hins vegar verður að nota kostnaðarstöðum og deildir sem víddir í lykilskipulagi ef kostnaðarstöðum notaðir aðeins sem kostnaðaruppsöfnun og deildir eru notaðar fyrir tekjuskráningu.
-   Miðaðu mörg stigveldi fyrir rekstrarfélög ef þú hefur flóknar kröfur um skýrslugjöf um hagnað og tap.
-   Í einum lögaðila, ekki móta mörgum stigveldum fyrir sama málefni stigveldis.
-   Stofnaðu ekki stigveldi fyrir hvert málefni. Vanalega er aðeins hægt að nota eitt stigveldi fyrir margan tilgang. Til dæmis er hægt að úthluta einu stigveldi rekstrareiningar á allar reglur sem tengjast tilgangi.
-   Stofna samhæft stigveldi. Í stigveldi, öllum hnútum sem eru í sama fjarlægð úr rótarhnút eru skilgreindar sem stig. Í samhæfðu stigveldi, aðeins ein gerð rekstrareiningar getur átt sér stað á hverju stigi, og fjarlægð úr rótarhnút í hvert stig er samræmd. Ef undirskipuð stig er milli deild og lögaðila eða viðskiptaeiningar sem eru frátakara fyrirtæki getur verið nauðsynlegt til að stofna samhæft stigveldi.
-   Gerðu ekki líkan af sérstöku stigveldi rekstrareiningar ef skipulag lögaðila sem er einnig rekstrarskipulag þitt. Blandað stigveldi lögaðila og rekstrareiningar getur þjónað tilgangi beggja.
-   Áður en þú mótar helstu atburðarásir endurskipulagningar þarf að nota öruggar gildisdagsetningar stigveldisins til að framkvæma áhrifagreiningu og staðfestingarpróf.
-   Nota ham fyrir drög til að breyta stigveldi áður en ný útgáfa er birt í vinnsluumhverfi.
-   Takmarka fjölda fólks sem hefur leyfi til að bæta við eða fjarlægja stofnanir frá stigveldi í framleiðsluumhverfi. Lægri tala minnkar hættuna sem á dýrum mistökum og gera verður leiðréttingar.

