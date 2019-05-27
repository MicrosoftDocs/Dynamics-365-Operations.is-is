---
title: Setja upp stjórnun tilboða
description: Þetta efni lýsir því hvernig á að setja upp tilboð í Talent.
author: andreabichsel
manager: AnnBe
ms.date: 02/04/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-18
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7fa0e5d30c06db16e105631e492af022acfcfd66
ms.sourcegitcommit: 2b890cd7a801055ab0ca24398efc8e4e777d4d8c
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/07/2019
ms.locfileid: "1518265"
---
# <a name="set-up-offer-management"></a>Setja upp stjórnun tilboða 

[!include [banner](includes/banner.md)]

Þegar umsækjandi er fluttur í tilboðsstigið í Dynamics 365 for Talent: Attract þarftu að tryggja að hægt sé að búa til tilboð fyrir umsækjandann á fljótlegan hátt, þau samþykkt eftir þörfum og send út til umsækjanda. Vegna þess að flest tilboð eru staðlað getur það verið búið til úr endurnýtanlegum sniðmátum. Í Attract, eru öll tilboð rúllað í tilboðspakka, sem er safn af einni eða fleiri tilboðsskjölum. 

Í þessu efni er listi yfir öll þau skref sem stjórnandi Attract myndi fylgja til að setja upp mismunandi tilboðspakki sniðmát sem hluta af tilboðsstjórnunargetu í Attract. Notendur sem ekki hafa stjórnandi hlutverk hafa ekki aðgang að þessum möguleikum.

>[!NOTE]
> Tilboðsstjórnunarmöguleikar eru tiltækar sem hluti af biðbót við alhliða ráðningar.

## <a name="offer-data"></a>Tilboðsgögn 

Tilboðsgögn eru minnstu einingin innan sniðmáts tilboðspakkans. Dæmigerð tilboð samanstendur af venjulegu texta og gildasafni. Gildissviðin eru þau eina sem geta breyst á milli tilboðanna. Á meðan tilboðssköpunin stendur er mikilvægasti þáttur sem stofnandi tilboðs getur lagt áherslu á, að listinn yfir staðgengla tilboðsgagna sem eru til staðar í sniðmáti tilboðspakka. Til að setja upp tilboðsgögn skaltu gera eftirfarandi.

1.  Farðu í **Stjórnun tilboða**.

1.  Stækkaðu **Safnið** í vinstra yfirlitssvæðinu og farðu síðan á **Tilboðsgögn**.

    >[!NOTE]
    > Á **Tilboðsgögn** síðunni eru **Upplýsingar umsækjanda** og **Upplýsingar um starf** kafla. Attract veitir nokkra tilbúna staðgengla tilboðsgagna.
    
    > Það eru köflum á síðunni til að skipuleggja mismunandi staðgengla tilboðsgagna saman í rökréttum hópum. Þessar köflum geta hjálpað við viðhald á tilboðsgögnum og keyrslu gagna á meðan stofnun tilboða stendur.

1.  Til að búa til nýjan tilboðsgagnahluta skaltu smella á **Bæta við hluta** og slá inn einkvæmt heiti fyrir hlutann.

1.  Til að bæta staðgenglum tilboðsgagna við hvaða hluta sem er skaltu smella á **Bæta við tilboðsgögnum** og sláðu inn einkvæmt heiti fyrir staðgengilinn.

1.  Til að breyta heiti hvaða hluta, settu bendilinn yfir heiti hlutans og uppfæra heitið.

1.  Til að breyta nafni fyrirliggjandi staðgengla tilboðsgagna, skaltu fyrst ganga úr skugga um að staðgengillinn sé ekki hluti af sniðmáti. Settu bendilinn yfir staðgengil tilboðsgagnanna og uppfærðu nafnið eftir þörfum.

1. Til að eyða núverandi staðgengli tilboðsgagna skaltu fyrst ganga úr skugga um að staðgengillinn sé ekki hluti af öðru sniðmáti. Þá skaltu setja bendilinn yfir staðsetninguna og þegar ruslakörfutáknið birtist skaltu smella á ruslakörfuna staðgengli tilboðsgagnanna.
    >[!NOTE]
    > Þú getur séð hversu mörg sniðmát staðgengill tilboðsgagna er hluti af númervísinum við hliðina á hverja tilboðsgögn. 

1. Til að eyða einhverjum hluta skaltu setja bendilinn yfir heitið. Ef ekkert af staðgenglum tilboðsgagnanna í hlutanum birtist í hvaða sniðmáti sem er, getur þú smellt á ruslakörfutáknið til að eyða því. 
    >[!NOTE]
    > Ef þú eyðir hlutanum mun einnig eyða öllum staðgenglum tilboðsgagnanna í þessum hluta.

Eftir að staðgenglar tilboðsgagnanna hafa verið settir upp, geturðu notað þau yfir hvaða sniðmát skjals sem er. Staðgenglar tilboðsgagna eru ekki bundin við tiltekið sniðmát - sama sett er hægt að nota á öllum sniðmátum.

## <a name="offer-data-rules"></a>Reglur um tilboðsgögn

Flest fyrirtæki hafa reglur um hvernig tilboð verða að vera gerð. Til dæmis getur fyrirtækið krafist þess að samsetning hámarkslaun á ársgrundvelli fyrir tiltekna stað og starfsaldursstig verði að vera innan ákveðins sviðs eða að aðeins fáir tiltekin gildi séu mögulegar fyrir tilboðsstig fyrir nýja starfsmanninn. Attract styður nú allar slíkar gagnareglur með CSV-skrá.

Til að undirbúa gagnareglur CSV skrá skaltu gera eftirfarandi.

1.  Ákveðið tilboðsgögn fyrir reglussettið. Til dæmis, **Árslaun**.

1.  Tilgreindu háð staðgengilsgildi tilboðsgagna. Til dæmis, **Staðsetning starfs** og **Stig**.

1.  Tilgreindu dálka 1 og 2 sem **Staðsetning starfs** og **Stig**.

1.  Til að hlaða inn sviðsgildi, veldu dálka 3 og 4 **Árslaun**. Til að hlaða upp tilteknu gildi í staðinn fyrir svið, veldu aðeins dálk 3 **Árslaun**.

1.  Fylltu út Microsoft Excel skrána út frá nauðsynlegum hlutverkum.

1.  Gakktu úr skugga um að hver röð sé einstök blanda af öllum gildum sem settar eru saman.

1.  Vista skrána sem CSV sniði.

Til að hlaða upp regluskrá tilboðsgagnanna skaltu gera eftirfarandi.

1.  Farðu í **Stjórnun tilboða**.

1.  Stækkaðu **Safnið** hlutann í vinstra yfirlitssvæðinu og farðu síðan á **Reglur tilboðsgagna**.

1.  Smelltu á **Nýtt gagnasafn** til að birta **Hlaða upp** valmyndina.

1.  Tilgreinið einkvæmt heiti fyrir reglusettið og hladdu síðan upp vistað CSV skrá.

1.  Smellið á **Bæta við**.
    Reglusettið verður unnin í bakgrunni og þú verður tilkynnt í forritinu og í tölvupósti þegar það er lokið.

    Þú verður tilkynnt ef það eru villur meðan þú vinnur með upphleðslu. Þú getur síðan sótt villukladdann, lagaðu skrána og hlaðið henni aftur upp.

1.  Notaðu þrípunktahnappinn (**...**) valkostinn ef þú vilt hlaða niður reglusettinu og uppfæra gildasafnið. Eftir uppfærslu geturðu hlaðið skránni aftur upp.

1.  Þú getur eytt núverandi reglusetti ef staðsetningin sem er skilgreind er ekki notuð í öðru sniðmáti skjals.

>[!NOTE]
> - Hver staðgengill getur aðeins haft eitt einstakt sett af dálkum sem það er háð. Til dæmis, ef **Árslaun** er háð **Staðsetning starfs** og **Stig**, getur þú ekki hlaðið inn öðru reglusetti þar sem **Árslaun** er háð mismunandi settum dálkum.

> - Þú getur sótt sýnishorn af reglusettum tilboðsgagna á flipanum **Sýnishorn** á **Reglur um tilboðsgögn** síðu.

> - Þegar stofnandi tilboðs hnekkir gildum sem mælt er með í reglum um tilboðsgögn, er tilboðið merkt sem óhefðbundið og skipað verður samþykki fyrir vinnuflæði.

## <a name="document-templates"></a>Sniðmát skjals

Sniðmát tilboðsskjals getur hjálpað stjórnendum að búa til tilboðsbréf. Sniðmát tilboðsskjals er sambland af textanum sem verður hluti af tilboðinu ásamt skilgreindum staðgenglum tilboðsgagna. 

Til að búa til sniðmát tilboðsskjals skaltu gera eftirfarandi.

1.  Farðu í **Stjórnun tilboða**.

1.  Stækkaðu **Safnið** í vinstra yfirlitssvæðinu og farðu síðan á **Sniðmát**.

    **Sniðmát** síðunni birtir lista yfir sniðmát skjala sem þegar hafa verið skilgreind.

1.  Til að búa til nýtt sniðmát skjals skaltu smella á **Nýtt sniðmát**.

1.  Sláðu inn einkvæma heitið fyrir sniðmátið og smelltu **Búa til**.

1.  Notaðu textaritil fyrir sniðinn texta til að setja inn eða breyta innihaldi tilboðsskjalsins. Þú getur sett inn töflur, myndir og tengla með því að nota valkostina sem eru í boði efst á textaritlinum.

1.  Þú getur sett inn staðgengla tilboðsgagna í tilboðsskjalinu með:

    - Dragðu og slepptu frá hægri glugganum.

    - Festir staðgengil tilboðsgagna beint á sinn stað. Sláðu inn **\#** og byrjaðu síðan að slá inn heiti staðgengils tilboðsgagna. Valkostir birtast í fellilistanum. Smelltu eða ýttu á **Sláðu inn** til að setja inn staðgengil tilboðsgagna.

    >[!NOTE]
    > - Til að tengja staðgengil við sniðmát tilboðsskjalsins án þess að sýna umsækjanda gildi þess, settu bendilinn yfir staðgengil tilboðsgagna og smelltu á **Festa** táknið. Þetta mun ýta staðgenglinum í **Fest tilboðsgögn** hluta sniðmáts tilboðsgagnanna. Til að taka burt skaltu fylgja sömu skrefum en smelltu **Taka burt** í listanum yfir staðgengla tilboðsgagna.

    > - Til að skoða lista yfir virka staðgengla tilboðsgagna, skipta yfir í **Virk** flipann hægra megin í glugganum.

    > - Ef þú setur inn staðgengil sem er keyrður af reglusetti fyrir tilboðsgögn getur þú séð tengingu þess staðgengils tilboðsgagna á öðrum gildum.

    > - Einnig er hægt að **Flytja inn** efni úr .docx skrá á þinni vél og breyta eftir þörfum. Þannig þarftu ekki að slá inn allt innihald í ritlinum.

1. Til að forskoða tilboðsskjalið er notað **Forskoðun** kost efst á síðunni.

1. Til að stjórna hvort stofnandi tilboðs getur breytt innihaldi tilboðsskjalsins skaltu nota **Stjórna heimild** valkostinn efst á síðunni. Ef þú vilt að stofnandi tilboðsins setji aðeins staðgengilsgildi og ekki breytt texta skaltu stilla heimildargildið í **Nei**.

1. Smelltu á **Vista** til að vista framfarir þínar. Sniðmátið verður vistað í stöðunni drög.

1. Til að ljúka og merkja skjalið sem birt er skaltu smella á **Ljúka**.

1. Þú getur séð hvaða sniðmát skjala eru virk, í ham fyrir drög og verið geymd og eru ekki lengur í notkun í lendingarupplifun skjalasafns sniðmáta.

>[!NOTE]
> Þú getur eytt öllum sniðmátum tilboðsskjala sem bjóða upp á núverandi sniðmát tilboðspakka.


## <a name="offer-package-templates"></a>Sniðmát tilboðspakka

Tilboðspakkar eru tilboðsgervingar sem eru deilt með umsækjanda og samanstanda af blöndu af einu eða fleiri sniðmátum tilboðsskjala. Til að búa til tilboðspakka skaltu gera eftirfarandi.

1.  Farðu í **Stjórnun tilboða**.

1.  Farðu í **Pakkar** frá vinstra yfirlitssvæðinu.

    Listi yfir virk pakkasniðmát sem eru tiltæk fyrir stofnendur tilboða til að nota birtist.

1.  Til að búa til nýja tilboðspakka skaltu smella á **Nýr pakki**.

1.  Sláðu inn einkvæmt heiti og smelltu **Búa til**.

1.  Smelltu **Bæta við sniðmáti**.

    >[!NOTE]
    > - Þú getur valið að búa til nýtt sniðmát eða velja úr núverandi.

    > - Ef þú velur að bæta við núverandi sniðmáti þarftu að ganga úr skugga um að sniðmát tilboðsskjalsins hafi verið vistað, lokað og merkt sem virkt.
    
    > - Þú getur valið eins mörg sniðmát skjala eins og þú vilt. 
    
1.  Smelltu **Lokið** til að fara aftur í **Pakkastjórnun**.

    Þú getur stillt röð skjala og einnig merkt hvort tiltekins tilboðsskjals sé krafist við stofnun tilboðs. Stofnandi tilboðs mun hafa möguleika á að eyða skjölum sem merktar eru sem **Ekki krafist**.

1. Til að vista sniðmátt tilboðspakkans svo að það sé nothæft af öllum stofnendum tilboða skaltu smella á **Vista og birta**.

   Til að skoða drög að sniðmátum tilboðspakka, farðu á flipann **Drög**. Ef breyting er gerð á tilboðspakka sniðmátið verður það að vera vistað og endurútgefið.

## <a name="configure-an-offer-process"></a>Stilltu tilboðsferli

Það eru nokkrir hlutar stofnunarferlis tilboðs sem hægt er að stilla af stjórnanda Attract.

- **Samþykki tilboða** - Veldu hvort samþykki tilboða sé krafist áður en tilboðið er hægt að senda til umsækjanda. Sem stjórnandi getur þú einnig ákveðið hvort öll samþykki tilboðs muni gerast í röð eða samhliða samþykki vinnuflæði. Þú getur einnig valið hvort samþykktaraðilar tilboðs eigi að bæta við athugasemdum ásamt samþykki þeirra fyrir tilboði. Samþykki tilboða eru nauðsynleg fyrir alla óhefðbundna tilboð.

- **Tilboðsupplifun umsækjanda**- Sem stjórnandi getur þú valið að stilla hvort öll tilboð séu með lokadag, og ef svo er, hvaða sjálfgefni mótlykill fyrir lokadag ætti að vera. Þú getur einnig stillt hvort umsækjendur geta hafnað tilboðinu.

- **Rafrænar undirskriftir** - Sem stjórnandi getur þú einnig valið aðferðina sem umsækjendur geta notað til að undirrita tilboð.
    - Adobe Sign - Allir tilboðspakkar verða sendir og undirritaðir með Adobe Sign. Stofnendur tilboða sem gefur út tilboðið verða að hafa Adobe Sign reikninginn sinn tengdan við Attract. Fyrir Adobe Sign-leyfi og ókeypis prufuútgáfu skal heimsækja [tengill](https://acrobat.adobe.com/us/en/business/integrations/microsoft-dynamics-365-for-talent.html).

    - DocuSign - Allir tilboðspakkar verða sendir og undirritaðir með DocuSign. Stofnendur tilboða sem gefur út tilboðið verða að hafa DocuSign reikninginn sinn tengdan við Attract. 
    
    - ESign - Þetta er sjálfgefinn valkostur, sem fylgir beint úr kassanum, þar sem notandinn getur skrifað undir tilboð með því að slá inn nafn og upphafsstafi.


Til að læra meira um stofnunarferli tilboðs, sjá [Stofna, samþykkja og undirrita tilboð](./creating-offers.md).
