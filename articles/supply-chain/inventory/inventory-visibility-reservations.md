---
title: Frátekningar Inventory Visibility
description: Þessi grein lýsir því hvernig á að setja upp pöntunareiginleikann til að búa til pantanir, neyta bókana og/eða afpanta tiltekið birgðamagn með því að nota Birgðasýnileika.
author: yufeihuang
ms.date: 11/04/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yufeihuang
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 0ae0589f8bac7ebf9b43cf0f3bc02680d324b29b
ms.sourcegitcommit: 49f8973f0e121eac563876d50bfff00c55344360
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 11/14/2022
ms.locfileid: "9762723"
---
# <a name="inventory-visibility-reservations"></a>Frátekningar Inventory Visibility

[!include [banner](../includes/banner.md)]

Þessi grein lýsir dæmigerðu notkunartilviki fyrir mjúkar frátekningar og útskýrir hvernig á að setja þær upp í Birgðasýnileika. Það felur í sér upplýsingar um hvernig á að búa til mjúkar frátekningar, jafna þær við líkamlega neyslu og aðlaga eða taka frá tiltekið birgðamagn.

## <a name="sample-use-case-for-soft-reservation"></a>Dæmi um notkunarhylki fyrir mjúkan fyrirvara

Mjúkir fyrirvarar hjálpa fyrirtækjum að ná einum sannleikauppsprettu fyrir tiltækar birgðir, sérstaklega meðan á pöntunarferlinu stendur. Þessi virkni er gagnleg fyrir stofnanir þar sem eftirfarandi skilyrði eru fyrir hendi:

- Fyrirtækið hefur að minnsta kosti tvö mismunandi kerfi sem taka beint við pöntunum á útleið.
- Stofnunin er mjög ströng og vill koma í veg fyrir tvíbókun á vörubirgðum sem getur gerst ef mörg kerfi geta yfirbókað síðasta lagerinn. Þessu ástandi er komið í veg fyrir þegar öll pöntunarkerfi geta hringt tafarlaust mjúk pöntunar-API símtöl til birgðasýnileika, sem veitir eina sannleiksuppsprettu fyrir framboð á birgðum.

[<img src="media/inventory-visibility-soft-reservation.png" alt="Inventory Visibility soft reservation." title=" Birgðasýnileiki mjúkur frágangur" width="720" />](media/inventory-visibility-soft-reservation.png)

Fyrri mynd sýnir hvernig mjúkur frágangur virkar og undirstrikar eftirfarandi aðgerðir:

- Upphaflegt birgðastig þitt er samstillt við Birgðasýnileika frá Microsoft Dynamics 365 Supply Chain Management.
- Mjúkar frátekningar eru settar frá hverri pöntunarrás þinni eða kerfum í Birgðasýnileika. Birgðasýnileiki staðfestir framboð á birgðum og reynir að gera mjúka frátekningu. Ef mjúk frátekt tekst, bætist birgðasýnileiki við mjúkt frátekið magn, dregur frá magni sem er tiltækt fyrir frátekningu (AFR) og svarar með mjúku fráteknu auðkenni.
- Á þessum tíma er birgðamagn þitt óbreytt.
- Síðan er hægt að samstilla annaðhvort stakar eða samanlagðar mjúk-fráteknar pantanir (pöntunarlínur) inn í Supply Chain Management til að gera erfiðar bókanir og losa í vöruhúsið eða uppfæra endanlegt birgðamagn.
- Þú getur stillt kerfið á [vega á móti mjúkum fyrirvörum](#offset-scm) þegar efnisbirgðir eru uppfærðar í Supply Chain Management.

Mjúkar bókanir eru venjulega búnar til, notaðar og afturkallaðar með því að nota API símtöl í birgðasýnileikaþjónustuna.

> [!NOTE]
> Þú getur valfrjálst sett upp Supply Chain Management (og önnur kerfi þriðju aðila) til að vega sjálfkrafa upp á móti magni sem hefur verið frátekið með því að nota Birgðasýnileika. Magni mótbókunar er eytt úr færslum frátekninga í birgðasýnileika.
>
> Sjálfgefið er að kveikt er á offset-aðgerðinni sjálfkrafa þegar þú kveikir á mjúka bókunareiginleikanum.

## <a name="turn-on-and-set-up-the-reservation-feature"></a><a name="turn-on"></a>Kveikja á og setja upp eiginleika frátekningar

Til að kveikja á eiginleika frátekningar skal fylgja þessum skrefum.

1. Skrá inn Power Apps og opið **Birgðasýnileiki**.
1. Opnaðu síðuna **Skilgreining**.
1. Í flipanum **Eiginleikastjórnun** skal kveikja á eiginleikanum *OnHandReservation*.
1. Skráðu þig inn í Supply Chain Management umhverfið þitt.
1. Farðu á **[Vinnusvæði eiginleikastjórnunar](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md)** og virkjaðu eiginleikann *Samþætting birgðasýnileika með mótbókun frátekningar* (krefst útgáfu 10.0.22 eða síðar).
1. Farðu í **Birgðastjórnun \> Uppsetning \> Færibreytur vegna samþættingar birgðasýnileika**, opnaðu flipann **Mótbókun frátekningar** og gerðu eftirfarandi stillingar:

    - **Virkja mótbókun frátekningar** – Stilltu á *Já* til að virkja þessa virkni.
    - **Frátekningarjafnari** – Veldu birgðafærslustöðuna sem mun vega upp á móti fráteknum sem eru gerðar í Birgðasýnileika. Þessi stilling ákvarðar stöðu pöntunarúrvinnslu sem setur af stað mótbókanir. Staða á birgðafærslu pöntunar sér um að rekja stigið. Veljið eitt af eftirfarandi gildum:

        - *Á pöntun* – Pantanir sem eru með *Á pöntun* stöðu mun senda mótvægisbeiðni þegar þau eru búin til. Á móti magni verður magn stofnaðrar pöntunar (lína).
        - *Áskilið* – Pantanir sem hafa a *Áskilið* staða mun senda mótvægisbeiðni þegar þau eru annaðhvort frátekin eða líkamlega frátekin. Þegar þú jafnar á *Áskilið* stöðu, mun pöntunin senda jöfnunarbeiðni við hvaða nýja birgðastöðu sem er næst fráteknum tíndum (til dæmis tínslu, fylgiseðli bókaður eða reikningsfærður). Þessi hegðun á sér stað jafnvel þótt þú sleppir frátektinni í Supply Chain Management og heldur áfram í aðra birgðastöðu (til dæmis ef þú sleppir frá losun í vöruhús til að tína og pakka). Beiðnin verður aðeins kveikt einu sinni. Ef það hefur verið virkjað við tínslu mun það ekki afrita jöfnunina þegar fylgiseðill er bókaður. Jöfnunarmagnið verður það sama og magn birgðafærslustöðunnar þegar jöfnunin var sett af stað (með öðrum orðum, *Frátekið pantað*/*Reserve Physical*, eða síðari stöðu, á samsvarandi pöntunarlínu).

1. Skráðu þig aftur inn í Inventory Visibility appið, farðu í **Stillingar** síðu og síðan á **Mjúk fyrirvara** flipa, skoðaðu sjálfgefna mjúka pöntunarstigveldið. Bættu nýjum víddum við stigveldið eftir þörfum.
1. Í **Stilltu Soft Reservation Mapping** kafla, skoða sjálfgefnar stillingar. Sjálfgefið er að mjúkt frátekið birgðamagn verður skráð á móti`softreservephysical` líkamlegur mælikvarði á gagnagjafann `iv`. The *Hægt að panta* reiknað mælikvarði er kortlagt til `availabletoreserve`. Ef þú vilt uppfæra`availabletoreserve` reiknuð mælikvarði, farðu í **Stillingar** síðu og síðan á **Reiknaður mælikvarði** flipa, stækkaðu og breyttu reiknaða mælikvarðanum.

Frekari upplýsingar er að finna í [Stilla birgðasýnileika](inventory-visibility-configuration.md).

> [!NOTE]
> Frátekningarstigveldið útskýrir röð vídda sem þarf að tilgreina þegar frátekningar eru gerðar. Það virkar á sama hátt og vísitölustigveldið virkar fyrir fyrirspurnir á staðnum, en það er notað sjálfstætt þannig að notendur geta tilgreint víddarupplýsingar til að gera nákvæmari fyrirvara.
>
> Mjúka bókunarstigveldið þitt ætti að innihalda`SiteId` og`LocationId` sem íhlutir, vegna þess að þeir búa til skiptingarstillingu birgðasýnileika.

Frekari upplýsingar um hvernig á skilgreina frátekningar er að finna í [Skilgreining frátekningar](inventory-visibility-configuration.md#reservation-configuration).

## <a name="use-the-reservation-feature-in-inventory-visibility"></a>Nota eiginleika frátekningar í birgðasýnileika

Þegar þú kallar á API frátekningar merki kerfið frátekningu tiltekins varnings og magns.

Hér er dæmi um atburðarás og sýnishorn af API fyrirspurnarhluta. Fyrirtækið Contoso selur vöru D0002 (Cabinet) frá rafrænum viðskiptavefsíðu sinni. Viðskiptavinur leggur inn sölupöntun fyrir lítinn rauðan skáp í gegnum vefsíðuna. Contoso ákveður að uppfylla þessa röð með því að nota eftirfarandi víddir:

- Auðkenni stofnunar = usmf
- Síða = 1
- Vöruhús = 11
- Vara = D0002
- Litur = rauður
- Stærð = lítill

Contoso hefur þegar sett upp API tengingu við Inventory Visibility frá sínu eigin rafrænu viðskiptakerfi. Þegar pöntunin er móttekin kallar kerfið samstundis á API til að gera mjúka frátekningu fyrir skápinn í Birgðasýnileika.

### <a name="create-soft-reservations-using-the-reservation-api"></a>Búðu til mjúkar bókanir með því að nota bókunar-API

Frátekningar eru gerðar í þjónustu birgðasýnileika með því að senda bókunarbeiðni á vefslóð þjónustunnar, t.d. `/api/environment/{environmentId}/onhand/reserve`.

Fyrir frátekningu verður meginmál beiðninnar að innihalda auðkenni fyrirtækis, afurðarkenni, frátekið magn og víddir.

Þegar þú kallar á API frátekningu er hægt að stjórna staðfestingu frátekningar með því að tilgreina Boolean `ifCheckAvailForReserv` færibreytu í meginmáli beiðninnar. Gildi `True` þýðir að staðfesting sé nauðsynleg og á móti merkir gildið `False` að staðfestingin er ekki nauðsynleg. Sjálfgefið gildi er `True`.

Ef þú vilt hætta við frátekningu eða afturkalla frátekningu á tilgreindu birgðamagni skaltu stilla magnið á neikvætt gildi og stilla `ifCheckAvailForReserv` færibreytuna á `False` til að sleppa villuleitinni.

Hér er dæmi um beiðnina sem vísar til sölupöntunarinnar í fyrra samhengi.

```json
# Url

#Replace {endpoint} with your system endpoint.
    {endpoint}/api/environment/{environmentId}/onhand/reserve

# Method
Post

# Header
# replace {access_token} with the one get from security service
Api-version: "1.0"
Content-Type: "application/json"
Authorization: "Bearer {access_token}"

# Body
{
    "id": "Testrequest-0005",
    "organizationId": "usmf",
    "productId": "D0002",
    "dimensions": {
        "SiteId": "1",
        "LocationId": "11",
        "ColorId": "red",
        "SizeId": "small"
    },
    "quantityDataSource": "iv",
    "modifier": "softreservphysical",
    "quantity": 1,
    "ifCheckAvailForReserv": true
}
```

Vel heppnuð mjúk bókunarbeiðni skilar a *mjúk bókunarauðkenni* fyrir hverja bókunarskrá. Mjúka frátekningarauðkennið er ekki einkvæmt auðkenni fyrir einstaka mjúka frátekningarfærslu, heldur sambland af auðkenni vöru og víddargildum sem tengjast mjúku fráteknu beiðninni. Þú getur skráð mjúka bókunarauðkennið á pöntunarlínunni þegar þú samstillir pantanir sem tókst að panta við Supply Chain Management eða annað ERP kerfi fyrir mótvægi.

### <a name="offset-soft-reservations-in-supply-chain-management"></a><a name="offset-scm"></a> Jafna mjúka fyrirvara í birgðakeðjustjórnun

Hægt er að jafna á móti mjúku fráteknu magni eftir að magnið í pöntun hefur verið dregið líkamlega frá í Supply Chain Management eða öðru ERP kerfi. Birgðasýnileiki býður upp á mjúka frátekningarjöfnun samþættingu við Supply Chain Management.

Fylgdu þessum skrefum til að vega upp á móti mjúkri frátekningu.

1. Skráðu þig inn í Supply Chain Management.
1. Fara til **Sala og markaðssetning \> Sölupantanir \> Allar sölupantanir**.
1. Í aðgerðarúðunni velurðu **Nýtt**.
1. Búðu til ytri sölupöntunina aftur og bættu við sölulínu sem notar nákvæmlega sama vöruauðkenni, skipulag, vefsvæði, vöruhús og víddargildi.
1. Á **Sölupöntunarlínur** Flýtiflipi, veldu sölulínuna sem þú varst að slá inn og veldu síðan á tækjastikunni **Birgðir \> Bókunarauðkenni**.
1. Fylgið einu af eftirfarandi skrefum:

    - Afritaðu mjúka bókunarauðkennið í mjúku bókunarbeiðnisvarinu þínu og límdu það inn í **Bókunarauðkenni** sviði.
    - Skildu eftir **Bókunarauðkenni** reiturinn auður, en veldu **Sjálfvirk jöfnun birgðaþjónustu** gátreit. Kerfið mun sjálfkrafa ákvarða hvaða vöru- og vöruvíddir á að vega á móti, byggt á vöruauðkenni og víddargildum sem eru færð inn á valda línu.

1. Veldu **Í lagi**.
1. Á meðan sama sölulínan er enn valin skaltu panta pantað magn líkamlega með því að velja **Birgðir \> Fyrirvari** á tækjastikunni á **Sölupöntunarlínur** Hraðflipi.
1. Ef þú hefur áður stillt **Frátekningarjafnari** sviði til *Frátekið*, þá kemur mótvægið af stað þegar pöntunarlínan hefur stöðuna *Reserve líkamlega* eða *Vara pantað*. Runuvinna keyrir einu sinni á mínútu til að samstilla mótvægisbeiðnir frá birgðakeðjustjórnun við birgðasýnileika.

> [!NOTE]
> Fyrir færslustöður sem innihalda tiltekinn varahlutjöfnunarbreytingar mun færsluuppfærslan vega á móti samsvarandi frátekningarskrá þegar öll eftirfarandi skilyrði eru uppfyllt:
>
> - Bókunarauðkenni birgðafærslunnar samsvarar bókunarauðkenni pöntunarfærslunnar í Birgðasýnileika.
> - Víddir birgðafærslunnar passa við víddir frátektarfærslunnar í Birgðasýnileika.
> - Breytingar á stöðu birgðafærslu kveikir á mótbókun fyrir frátekningar þegar staða birgðafærslu endurspeglar þá staðreynd að pöntunarferlinu sé lokið eða því sleppt.

Jöfnunarmagn fylgja birgðamagninu sem tilgreint er á viðkomandi birgðafærslum. Jöfnun mun aðeins taka gildi ef frátekið magn er eftir í Birgðasýnileika.

### <a name="cancel-or-revert-a-soft-reservation"></a>Hætta við eða afturkalla mjúka pöntun

Ef upprunalegri pöntunarlínu er hætt við eða henni eytt og þú verður að afturkalla samsvarandi mjúka frátekningu skaltu bóka neikvætt magn sem hefur nákvæmlega sömu upplýsingar í meginmáli API fyrirspurnarinnar.
