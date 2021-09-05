---
title: GS1-strikamerki og QR-kóðar
description: Í þessu efnisatriði er lýst hvernig setja á upp GS1 strikamerki og QR-kóða svo hægt sé að skanna merkingar í vöruhúsi.
author: Mirzaab
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: ef28fcaf308225a78bcbac42f591e6b24b21b1b1
ms.sourcegitcommit: 2b04b5a5c883d216072bb91123f9c7709a41f69a
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/16/2021
ms.locfileid: "7384538"
---
# <a name="gs1-bar-codes-and-qr-codes"></a>GS1-strikamerki og QR-kóðar

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Vöruhússtarfsmenn þurfa oft að ljúka nokkrum verkefnum þegar þeir nota skanna fyrir farsíma til að skrá hreyfingar vöru, spjalds eða geymis. Þessi verkefni geta falið í sér bæði að skanna strikamerkingar og færa inn upplýsingar handvirkt í fartækið. Strikamerkin nota tiltekið snið fyrirtækis sem þú skilgreinir og stjórnar með Microsoft Dynamics 365 Supply Chain Management.

GS1 strikamerki og QR-kóði fyrir flutningsmerki voru þróuð til að bjóða upp á alþjóðlegan staðal fyrir gagnaskipti á milli fyrirtækja. GS1 snið kóða ekki aðeins gögnin heldur leyfa þér einnig að nota fyrirfram skilgreindan lista af auðkennum *forrita* til að skilgreina merkingu gagnanna. GS1 staðallinn skilgreinir gagnasniðið og ýmis konar gögn sem hægt er að nota til að kóða. Ólíkt eldri strikamerkjum geta GS1 strikamerki haft marga gagnaþætti. Þess vegna getur ein skönnun á strikamerkjum náð yfir nokkrar tegundir vöruupplýsinga, eins og lotuna og fyrningardagsetninguna.

GS1 stuðningur í Supply Chain Management einfaldar verulega skönnunarferlið í vöruhúsum þar sem bretti og geymar eru merkt með því að nota kóða á GS1 sniði. Vöruhússtarfsmenn geta dregið út allar nauðsynlegar upplýsingar með einni skönnun á GS1 strikamerki. Með því að útiloka nauðsyn þess að gera margar skannanir og/eða slá inn upplýsingar handvirkt, hjálpa GS1 strikamerkin til við að minnka tímann sem tengist verkefnum. Um leið hjálpa þau einnig til við að bæta nákvæmni.

Skipulagsstjórar verða að setja upp nauðsynlegan lista yfir auðkenni forrita og tengja hvert þeirra við viðeigandi valmyndaratriði fyrir fartæki. Þá er hægt að nota auðkenni forritsins yfir vöruhús sem alhliða stillingu fyrir flutning og pökkun. Þess vegna munu allir merkimiðar fara fram á sameinuðu eyðublaði.

Nema annað sé tekið fram notar þetta umræðuefni hugtakið *strikamerki* til að vísa bæði til strikamerkja og QR-kóða.

## <a name="turn-on-the-gs1-feature"></a>Kveikja á GS1-eiginleikanum

Áður en hægt er að nota þennan eiginleika þarf að kveikja á honum í kerfinu. Stjórnendur geta notað stillingarnar [eiginleikastjórnun](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til að athuga stöðu eiginleikans og kveikja á honum. Á vinnusvæðinu **Eiginleikastjórnun** er eiginleikinn tilgreindur á eftirfarandi hátt:

- **Eining:** *Vöruhúsakerfi*
- **Heiti eiginleika:** *Skanna GS1-strikamerki*

## <a name="set-up-global-gs1-options"></a>Setja upp altæka valkosti GS1

Síðan **Færibreytur Warehouse Management** býður upp á nokkrar stillingar sem setja á altæka valkosti GS1.

Til að setja upp altæka valkosti GS1 skal fylgja þessum skrefum.

1. Farðu í **vöruhúsakerfi \> Uppsetning \> Færibreytur vöruhúsakerfis**.
1. Á flýtiflipanum **Strikamerki** stillirðu eftirfarandi reiti.

    - **FNC1-stafur** – Tilgreindu stafi sem á að túlka sem forskeyti þegar strikamerki er þáttað.
    - **Stafur gagnafylkis** – Tilgreindu stafi sem á að túlka sem forskeyti þegar gagnafylki er þáttað.
    - **Stafur QR kóða** – Tilgreindu stafi sem á að túlka sem forskeyti þegar QR-kóði er þáttaður.
    - **Skiltákn fyrir hópa** Tilgreinið þann staf sem ber kennsl á aðskilda hluta strikamerkis eða QR-kóða.
    - **Hámarkslengd auðkennis** – Tilgreinið hámarksfjölda stafa sem leyfilegt er að nota fyrir auðkenni forritsins.

> [!NOTE]
> Forskeyti segja kerfinu að strikamerki sé dulkóðað samkvæmt GS1-staðlinum. Hægt er að nota allt þrjú forskeyti (**FNC1-staf**, **Staf gagnafylkis** og **QR-kóðastaf**) saman og af ýmsum ástæðum.

## <a name="gs1-application-identifiers"></a>Kennimerki GS1 forrits

GS1 snið kóða ekki aðeins gögnin heldur leyfa þér einnig að nota fyrirfram skilgreindan lista af auðkennum forrita til að skilgreina merkingu gagnanna. Skipulagsstjórar verða að setja upp nauðsynlegan lista yfir auðkenni forrita og tengja hvert þeirra við viðeigandi valmyndaratriði fyrir fartæki. Auðkennin er síðan hægt að nota á milli vöruhúsa sem alhliða stillingu fyrir flutning og pökkun. Þess vegna munu allir merkimiðar fara fram á sameinuðu eyðublaði.

Kerfið notar gögnin, einkum fyrirfram skilgreind auðkenni forrita, til að setja reglur sem eiga að gilda um viðeigandi skannaðar upplýsingar.

Hvert auðkenni forritsins gefur kerfinu merki um að síðari stafir í skannaða strikamerkinu skuli teljast blokk dulkóðaðra upplýsinga. Uppsetning auðkenna forritsins skilgreinir hvernig kerfið á að túlka strikamerki og vista það sem gildi í kerfinu.

Skipulagsstjórar geta notað stöðluð alþjóðleg forritaskilríki og/eða búið til sín eigin.

### <a name="load-the-standard-application-identifiers"></a>Sækja staðlað forritsauðkenni

Til að hefjast handa á skjótan hátt er hægt að hlaða inn lista yfir algeng alþjóðleg auðkenni forrits. Þú getur síðan víkkað eða breytt listanum síðar eins og þú krefst.

Til að hlaða inn stöðluðum kennimerkjum forrita skal fylgja þessum skrefum.

1. Farðu í **Warehouse Management \> Uppsetning \> GS1 \> GS1 auðkenni forrits**.
1. Á aðgerðasvæðinu skal velja **Stofna sjálfgefna uppsetningu**:

> [!WARNING]
> Skipunin **Stofna sjálfgefna uppsetningu** eyðir öllum núverandi skilgreindum auðkennum forrits og skiptir þeim út fyrir hefðbundna listann. Eftir að þú hleður inn sjálfgefinni uppsetningu getur þú hins vegar sérsniðið listann eins og þú vilt.

### <a name="set-up-custom-application-identifiers"></a>Setja upp sérsniðin auðkenni forrita

Ef sum eða öll auðkenni forrita sem fyrirtækið notar eru frábrugðin staðalsafninu er hægt að búa til eigin kóða frá grunni eða sérsníða staðalsafnið eftir þörfum.

Til að setja upp og sérsníða eigin GS1 forritsauðkenni skal fylgja eftirfarandi skrefum.

1. Farðu í **Warehouse Management \> Uppsetning \> GS1 \> GS1 auðkenni forrits**.
1. Fylgið einu af eftirfarandi skrefum:

    - Til að búa til nýtt auðkenni: Veldu **Nýtt** á aðgerðasvæðinu.
    - Til að breyta auðkenni sem þegar er til: Veldu auðkennið og veldu svo **Breyta** á aðgerðasvæðinu.

1. Stilltu eftirfarandi reiti fyrir nýja eða valda auðkennið:

    - **Kennimerki forrits** – Færðu inn auðkenniskóðann fyrir kennimerki forritsins. Venjulega er þessi kóði tveggja stafa heiltala en getur verið lengri. Fyrir tugabrot segir síðasti tölustafurinn til um fjölda aukastafa. Nánari upplýsingar er að finna í lýsingu gátreitsins **Aukastafur** síðar í þessum lista.
    - **Lýsing** – Færðu inn stutta lýsingu á kennimerkinu.
    - **Föst lengd** – Veldu þennan gátreit ef gildi sem eru skönnuð með því að nota þetta kennimerki forrits eru með fastan fjölda stafa. Hreinsa þennan gátreit ef lengd gilda er breytileg. Í því tilviki þarf að gefa upp lok gildisins með því að nota skiltákn flokksins sem var tilgreint á síðunni **Færibreytur Warehouse Management**.
    - **Lengd** – Færðu inn hámarksfjölda stafa sem geta birst í gildunum sem eru skönnuð með því að nota kennimerki forritsins. Ef gátreiturinn **Föst lengd** er valinn er gert ráð fyrir nákvæmlega þessum fjölda stafa.
    - **Gerð** – Veldu gerð gildis sem er skannað með því að nota þetta kennimerki forrits (*Tölustafir*, *Bókstafir og tölur* eða *Dagsetning*). Fyrir dagsetningar er væntanlegt snið ÁÁMMDD (án bils eða bandstrika).
    - **Aukastafur** – Veldu þennan gátreit ef gildið inniheldur mögulegt tugabrot. Ef þessi reitur er valinn mun kerfið nota síðasta tölustaf kennimerkis forritsins til að ákvarða fjölda aukastafa. Til dæmis ef kennimerki forritsins er *3205* verða fimm stafir gildisins sem eru lengst til hægri túlkaðir þannig að þeir eigi að koma á eftir tugabrotinu.

> [!NOTE]
> Skiltákn fyrir hópa sem er tilgreint á síðunni **Færibreytur Warehouse Management** er valfrjálst ef gildi þar sem kennimerki forrits fylgir í kjölfarið er með fast lengd, eða ef lengdin er í hámarki (þ.e. ef lengdin jafngildir gildinu **Lengd** sem er stillt fyrir kennimerki forritsins).

## <a name="establish-the-generic-gs1-setup"></a>Hefja almenna GS1-uppsetningu

Með almennri GS1-uppsetningu er komið upp safni algengra varpana. Þessar varpanir stemma hvern viðeigandi innsláttarreit í fartækjaforritinu við kennimerki forritsins sem stýrir því hvernig túlka og geyma eigi gildi úr skönnuðum strikamerkjum í þeim reit. Þessar stillingar eiga sjálfgefið við um allar skannanir fyrir öll valmyndaratriði fartækis. Hins vegar er hægt að skrifa yfir þær fyrir einn eða fleiri tiltekna reiti með GS1-reglu sem er úthlutað á tiltekið valmyndaratriði.

Almenn uppsetning GS1 gerir aðeins kleift að skanna eitt gildi í einu. Ef þú þarft því að hlaða mörgum reitargildum úr einni skönnun þarftu að setja upp GS1-reglu fyrir viðeigandi valmyndaratriði.

Frekari upplýsingar um GS1-reglur er að finna í næsta hluta.

### <a name="load-the-standard-generic-gs1-setup"></a>Hlaða hefðbundna almenna uppsetningu GS1

Síðan **Almenn uppsetning GS1** gerir þér kleift að hlaða stöðluðu safni varpana á milli reita fartækis og staðlaðra kennimerkja forrits sem sjálfgefna uppsetningin býr til.

Til að setja upp almenna uppsetningu GS1 skal fara í **Warehouse Management \> Uppsetning \> GS1 \> Almenn uppsetning GS1**. Veldu síðan **Búa til sjálfgefna uppsetningu** til að úthluta sjálfkrafa viðeigandi kennimerki forrits í hvern reit sem er yfirleitt notaður af valmyndaratriðum fartækis.

> [!WARNING]
> Ef einhver almenn uppsetning GS1 er þegar til staðar mun skipunin **Stofna sjálfgefna uppsetningu** eyða henni að fullu og hlaða hefðbundnu uppsetningunni.

### <a name="customize-the-standard-generic-gs1-setup"></a>Sérsníða hefðbundna almenna uppsetningu GS1

Til að sérsníða almenna uppsetningu GS1 skal fylgja þessum skrefum.

1. Farðu í **Warehouse Management \> Uppsetning \> GS1 \> Almenn uppsetning GS1**.
1. Fylgið einu af eftirfarandi skrefum:

    - Til að búa til nýja vörpun: Veldu **Ný** á aðgerðasvæðinu.
    - Til að breyta núverandi vörpun: Veldu vörpunina og veldu svo **Breyta** á aðgerðasvæðinu.

1. Stilltu eftirfarandi reiti fyrir nýju eða völdu vörpunina:

    - **Reitur** – Veldu eða færðu inn færslureit fartækjaforritsins sem gildi á innleið á að vera úthlutað í. Gildið er ekki birtingarnafnið sem starfsmenn sjá. Í staðinn er það heiti lykils sem er úthlutað í reitinn í undirliggjandi kóða. Sjálfgefin uppsetning býður upp á safn reita sem eru líklegir til að koma að gagni og inniheldur einföld heiti lykla fyrir hvern reit og samsvarandi forritaða virkni. Hins vegar gæti þurft að ræða við þróunaraðila til að finna rétt val fyrir innleiðinguna.
    - **Kennimerki forrits** – Veldu viðeigandi kennimerki forrits eins og það er skilgreint á síðunni **GS1 kennimerki forrits**. Kennimerkið ákvarðar hvernig strikamerkið verður túlkað og geymt sem gildi fyrir nefndan reit. Eftir að þú hefur valið kennimerki forrits sýnir reiturinn **Lýsing** lýsingu á því.

## <a name="set-up-gs1-policies-that-you-can-assign-to-mobile-device-menu-items"></a>Setja upp GS1 reglur sem hægt er að úthluta til valmyndaratriða fyrir fartæki

Tilgangur GS1 staðalsins er að gera starfsmönnum kleift að hlaða inn nokkrum gildum þegar þeir skanna eitt strikamerki í einu. Til að ná þessu markmiði verða skipulagsstjórar að setja upp GS1 stefnu sem segir kerfinu hvernig á að túlka strikamerki með mörgum gildum. Seinna er hægt að setja reglur á valmyndaratriði fyrir fartæki til að stjórna því hvernig strikamerki er túlkað þegar starfsmenn skanna það á meðan þeir nota tiltekið valmyndaratriði.

Ef engin GS1 stefna er gefin í valmyndaratriði getur kerfið aðeins tekið eitt gildi. Þetta gildi er notað á inntak fartækjaforritsins sem er valið þegar starfsmaðurinn gerir skönnun, eins og almenn uppsetning GS1 tilgreinir. Ef GS1-stefnu er úthlutað á valmyndaratriðið notar kerfið enn almenna uppsetningu GS1 til að varpa fyrsta gildi strikamerkisins á valda reitinn. Hins vegar getur hún sótt fleiri reitargildi eins og tilgreint er af viðeigandi stefnu.

### <a name="load-the-standard-specific-gs1-policies"></a>Sækja staðlaðar sértækar GS1 stefnur

Þú getur hlaðið inn GS1-stefnu til að hefjast handa á skjótan hátt. Þú getur síðan víkkað út eða breytt stefnjunum síðar eftir hentisemi.

Til að hlaða inn stöðluðum kennimerkjum forrita skal fylgja þessum skrefum.

1. Farðu í **Warehouse Management \> Uppsetning \> GS1 \> GS1-stefna**.
1. Á aðgerðasvæðinu skal velja **Stofna sjálfgefna uppsetningu**:

> [!WARNING]
> Skipunin **Stofna sjálfgefna uppsetningu** eyðir öllum núverandi skilgreindum stefnum og skiptir þeim út fyrir hefðbundið safn af stefnum. Eftir að sjálfgefna uppsetningin hefur verið hlaðin er hins vegar hægt að sérsníða stefnurnar eftir þörfum.

### <a name="set-up-custom-specific-gs1-policies"></a>Setja upp sérstakar GS1-stefnur

Til að setja upp og sérsníða GS1-stefnurnar þínar skaltu fylgja þessum skrefum.

1. Farðu í **Warehouse Management \> Uppsetning \> GS1 \> GS1-stefna**.
1. Fylgið einu af eftirfarandi skrefum:

    - Til að búa til nýja stefnu: Veldu **Ný** á aðgerðasvæðinu.
    - Til að breyta fyrirliggjandi stefnu: Veldu hana í listaglugganum.

1. Í haus nýju eða völdu reglunnar skal stilla eftirfarandi gildi:

    - **Heiti reglu** – Færðu inn heiti fyrir regluna.
    - **Lýsing** – Færðu inn stutta lýsingu á reglunni.

1. Í flýtiflipanum fyrir neðan hausinn skal varpa reitarheitum í kennimerki forrits eins og þörf er á fyrir núverandi reglu. Notaðu hnappana á tækjastikunni til að bæta við eða fjarlægja línur eftir þörfum. Fyrir hverja línu skal stilla eftirfarandi reiti:

    - **Reitur** – Veldu eða færðu inn færslureit fartækjaforritsins sem gildi á innleið á að vera úthlutað í. Gildið er ekki birtingarnafnið sem starfsmenn sjá. Í staðinn er það heiti lykils sem er úthlutað í reitinn í undirliggjandi kóða. Sjálfgefin uppsetning býður upp á safn reita sem eru líklegir til að koma að gagni og inniheldur einföld heiti lykla fyrir hvern reit og samsvarandi forritaða virkni. Hins vegar gæti þurft að ræða við þróunaraðila til að finna rétt val fyrir innleiðinguna.
    - **Kennimerki forrits** – Veldu viðeigandi kennimerki forrits eins og það er skilgreint á síðunni **GS1 kennimerki forrits**. Kennimerkið ákvarðar hvernig strikamerkið verður túlkað og geymt sem gildi fyrir nefndan reit. Eftir að þú hefur valið kennimerki forrits sýnir reiturinn **Lýsing** lýsingu á því.
    - **Röðun** – Hvert strikamerki með mörgum gildum inniheldur röð af kennimerkjum forrits þar sem gildi fyrir hverju og einu þeirra. Viðeigandi GS1-regla ber kennsl á hvaða kennimerki forrits er varpað í sérhvern reit gagnagrunns. Ef strikamerki notar hinsvegar sama kennimerki forrits oftar en einu sinni notar kerfið röðina sem kennimerki forritsins birtast í kóðanum til að varpa þeim í reiti. Fyrir raðir sem deila auðkenni forrits með einni eða fleiri röðum skal nota þennan reit til að setja upp röðina sem samsvarandi raðir eru unnar í. Fyrst verður unnið úr þeirri röð sem hefur lægsta flokkunargildið.

> [!NOTE]
> Fyrir strikamerki sem innihalda fleiri en eitt eins kennimerki forrits *verður að* nota reitinn **Röðun** til að ákvarða röð reitanna.

## <a name="assign-gs1-policies-to-mobile-device-menu-items"></a>Úthluta GS1-reglum á valmyndaratriði fartækis

Sjálfgefið er að allir valmyndarhlutir fartækisins séu með innsláttarreiti þar sem starfsmenn geta skannað eitt gildi, í samræmi við almenna GS1 uppsetninguna. Ef þú vilt að starfsmenn geti skannað fleiri en eitt reitargildi í einni skönnun fyrir hvaða valmyndaratriði sem er fyrir fartæki verður þú að úthluta GS1-reglu með því að fylgja þessum skrefum.

1. Farðu í **Vöruhúsakerfi \> Uppsetning \> Fartæki \> Valmyndaratriði fartækis**.
1. Stofnaðu eða opnaðu valmyndaratriði.
1. Í flýtiflipanum **Almennt** skal stilla reitinn **GS1-regla** á þá relgu sem á við um valmyndaratriðið.

## <a name="gs1-setup-example"></a>Dæmi um uppsetningu GS1

Þetta dæmi á við um kerfi þar sem GS1-valkostir eru settir upp á eftirfarandi hátt:

- Á síðunni **Færibreytur Warehouse Management** eru eftirfarandi altækar stillingar settar á:

  - **FNC1-stafur** *\]C1*
  - **Skiltákn fyrir hópa:** *\~*

- Á síðunni **GS1 kennimerki forrits** eiga eftirfarandi kennimerki forrits við í þessu dæmi.

    | Kennimerki forrits | lýsing | Föst lengd | Lengd | Gerð | Tugabrot |
    |---|---|---|---|---|---|
    | 01 | GTIN | Valið | 14 | Tölugildi | Útleyst |
    | 10 | Rununúmer | Útleyst | 20 | Bókstafir og tölur | Útleyst |
    | 17 | Gildistími | Valið | 6 | Dagsetning | Útleyst |
    | 30 | Magn sem tekið er á móti | Útleyst | 8 | Tölugildi | Útleyst |

- Á síðunni **Almenn uppsetning GS1** eiga eftirfarandi stillingar fyrir almenna GS1-reglu við í þessu dæmi.

    | Svæði | Kennimerki forrits | lýsing |
    |---|---|---|
    | ItemId | 01 | GTIN |

- Á síðunni **GS1-regla** er regla þar sem reiturinn **Heiti reglu** er stilltur á *Móttaka innkaupa*. Þessi regla inniheldur eftirfarandi línur.

    | Svæði | Kennimerki forrits | lýsing | Röðun |
    |---|---|---|---|
    | ExpDate | 17 | Gildistími | 0 |
    | InventBatchId | 10 | Rununúmer | 0 |
    | Magn | 30 | Magn sem tekið er á móti | 0 |

- Á síðunni **Valmyndaratriði fartækis** er til valmyndaratriði sem heitir *Móttaka innkaupa*. Reiturinn **GS1-regla** er stilltur á *Móttaka innkaupa*.

Eftir að vörur í innkaupapöntun eru komnar í vöruhúsið fylgir starfskrafturinn þessum skrefum.

1. Á fartækinu skal velja valmyndaratriðið **Móttaka innkaupa**.
1. Sláðu inn innkaupapöntunarnúmerið.
1. Veldu reitinn **Vara** og skannaðu eftirfarandi strikamerki: *\]C10100000012345678\~3030\~10b1\~17220215*.

Kerfið þáttar skannaða strikamerkið með eftirfarandi hætti vegna stillinga sem eru settar upp í þessu dæmi.

| Reitarlykill | Kenni umsóknar | Virði | Nóta |
|---|---|---|---|
| ItemId | 01 | 00000012345678 | Vegna þess að starfsmaðurinn skannaði í reitnum **Vara** er fyrsta gildið í strikamerkinu varpað í þann reit. Vörpunin er tekin úr almennri uppsetningu GS1. |
| Magn | 30 | 30 | Vegna þess að verið er að sækja nokkur reitargildi í einni skönnun er þessi vörpun og allar næstu varpanir sóttar úr GS1-reglunni sem er úthlutað á valmyndaratriðið **Móttaka innkaupa**. Þetta gildi er magnið sem var móttekið. |
| InventBatchId | 10 | b1 | Þetta gildi er runukennið. |
| ExpDate | 17 | 220215 | Dagsetningarsniðið er ÁÁMMDD. Því er lokadagurinn 15. febrúar 2022. |

Kvittunin er síðan skráð og viðeigandi gildi gagnagrunnsins eru færð inn á eftir stöku skönnuninni.
