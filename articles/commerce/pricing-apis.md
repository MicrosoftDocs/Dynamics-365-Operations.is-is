---
title: API fyrir verðlagningu viðskipta
description: Þessi grein lýsir ýmsum verðlagningar-API sem eru veitt af Microsoft Dynamics 365 Commerce verðlagsvél.
author: boycez
ms.date: 08/10/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: boycez
ms.search.validFrom: 2022-07-15
ms.openlocfilehash: d694c44f6987fbf2a360869d2fb2a2fbaf0d2e4d
ms.sourcegitcommit: 924dbcdc6b03f6a7ae3a07378ec405fd15c7e359
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/13/2022
ms.locfileid: "9293652"
---
# <a name="commerce-pricing-apis"></a>API fyrir verðlagningu viðskipta

[!include [banner](../includes/banner.md)]

Þessi grein lýsir ýmsum verðlagningar-API sem eru veitt af Microsoft Dynamics 365 Commerce verðlagsvél.

The Dynamics 365 Commerce verðlagningarvél veitir eftirfarandi smásölumiðlara API sem hægt er að nota af utanaðkomandi forritum til að styðja við ýmsar verðtilvik:

- **GetActivePrices** – Þetta API fær útreiknað verð vöru, þar á meðal einfalda afslætti.
- **Reiknaðu Söluskjal** – Þetta API reiknar út verð og afslátt fyrir vörur í tilteknu magni ef þær eru keyptar saman.
- **GetAvailablePromotions** – Þetta API fær viðeigandi afslátt fyrir vörur í körfunni. 
- **AddCoupons** - Þetta API bætir afsláttarmiðum í körfu.
- **Fjarlægja afsláttarmiða** - Þetta API fjarlægir afsláttarmiða úr körfu.

Fyrir frekari upplýsingar um hvernig á að neyta Retail Server API í ytri forritum, sjá [Notaðu smásöluþjóna API í ytri forritum](dev-itpro/consume-retail-server-api.md).

## <a name="getactiveprices"></a>GetActivePrices

The *GetActivePrices* API var kynnt í útgáfu Commerce útgáfu 10.0.4. Þetta API fær útreiknað verð vöru, þar á meðal einfalda afslætti. Það reiknar ekki fjöllínuafslátt og það gerir ráð fyrir að hver vara í API beiðni hafi 1 magn. Þetta API getur einnig tekið lista yfir vörur sem inntak og spurt um verð einstakra vara í lausu.

The *GetActivePrices* API styður **Starfsmaður**, **·**, **·**, og **Umsókn** Verslunarhlutverk.

Helsta notkunartilvikið fyrir *GetActivePrices* API er vöruupplýsingasíðan (PDP), þar sem smásalar vilja sýna besta verðið fyrir vöru, þar á meðal virkan afslátt.

Eftirfarandi tafla sýnir inntaksfæribreytur fyrir *GetActivePrices* API.

| Nafn                                    | Undirnafn | Gerð | Áskilið/valfrjálst | Lýsing |
|-----------------------------------------|----------|------|-------------------|-------------|
| projectDomain                           | | ProjectionDomain | Áskilið | |
|                                         | ChannelId | Langt | Áskilið | |
|                                         | CatalogId | Langt | Áskilið | |
| vöruauðkenni                              | | IEtalanlegur\<long\> | Áskilið | Listi yfir vörur til að reikna verð fyrir. |
| Virkt Dagsetning                              | | DateTimeOffset | Áskilið | Dagsetningin þegar verð eru reiknuð út. |
| Skilríki viðskiptavinar                              | | strengur | Valfrjálst | Reikningsnúmer viðskiptavinarins. |
| affiliationLoyalty Tiers                 | | IEtalanlegur\<AffiliationLoyaltyTier\> | Valfrjálst | Tengsl og tryggðarþrep. |
|                                         | AffiliationId | Langt | Áskilið | Aðildarauðkenni. |
|                                         | LoyaltyTierId | Langt | Valfrjálst | Auðkenni vildarþrepsins. |
| Innihalda SimpleDiscountsInContextualPrice | | ból | Valfrjálst | Stilltu þessa færibreytu á **satt** að taka einfalda afslætti inn í verðútreikning. Sjálfgefið gildi er **rangt**. |
| Fela í sérVariantPriceRange                | | ból | Valfrjálst | Stilltu þessa færibreytu á **satt** til að fá lágmarks- og hámarksverð meðal allra afbrigða fyrir aðalvöru. Sjálfgefið gildi er **rangt**. |
| Fela í sérAttainablePricesAnd Discounts     | | ból | Valfrjálst | Stilltu þessa færibreytu á **satt** til að fá viðunandi verð og afslætti. Sjálfgefið gildi er **rangt**. |

**Dæmi um beiðnir**

```json
{
    "projectDomain": 
    {
        "ChannelId": 5637144592,
        "CatalogId": 0
    },
    "productIds": 
    [
        68719489871
    ],
    "activeDate": "2022-06-20T14:40:05.873+08:00",
    "includeSimpleDiscountsInContextualPrice": true,
    "includeVariantPriceRange": false
}
```

**Dæmi um svarhluti**

```json
{
    "value": 
    [
        {
            "ProductId": 68719489871,
            "ListingId": 68719489871,
            "BasePrice": 0,
            "TradeAgreementPrice": 0,
            "AdjustedPrice": 0,
            "MaxVariantPrice": 0,
            "MinVariantPrice": 0,
            "CustomerContextualPrice": 0,
            "DiscountAmount": 0,
            "CurrencyCode": "USD",
            "ItemId": "82000",
            "InventoryDimensionId": null,
            "UnitOfMeasure": "ea",
            "ValidFrom": "2022-06-20T01:40:05.873-05:00",
            "ProductLookupId": 0,
            "ChannelId": 5637144592,
            "CatalogId": 0,
            "SalesAgreementPrice": 0,
            "PriceSourceTypeValue": 1,
            "DiscountLines": [],
            "AttainablePriceLines": [],
        }
    ]
}
```

## <a name="calculatesalesdocument"></a>Reiknaðu Söluskjal

The *Reiknaðu Söluskjal* API var kynnt í útgáfu Commerce útgáfu 10.0.25. Þetta API reiknar út verð og afslátt fyrir vörur í tilteknu magni ef þær eru keyptar saman í pöntun. Verðreikningurinn á bak við *Reiknaðu Söluskjal* API tekur bæði til einnar línuafsláttar og fjöllínuafsláttar.

Helsta notkunartilvikið fyrir *Reiknaðu Söluskjal* API er verðútreikningur í tilfellum þar sem fullt körfusamhengi er ekki viðvarandi (svo sem sölutilboð). Sviðsmyndir á sölustöðum (POS) og rafræn viðskipti í viðskiptum geta einnig notið góðs af þessu notkunartilviki. Lægra heildarverð þegar vörur í körfu eru reiknaðar sem sett (til dæmis fyrir stakar búntir, tengdar eða ráðlagðar vörur eða vörur sem þegar hefur verið bætt í körfuna) gæti sannfært viðskiptavini um að bæta vörum í körfuna.

Gagnalíkanið fyrir bæði beiðnina og svarið *Reiknaðu Söluskjal* API er **Karfa**. Hins vegar, í samhengi við þetta API, er gagnalíkanið nefnt **Söluskjal**. Vegna þess að flestir eiginleikarnir eru valfrjálsir, og aðeins fáir þeirra hafa áhrif á verðútreikninginn, eru aðeins verðtengdir reitir sýndir í eftirfarandi töflu. Við mælum ekki með því að aðrir reitir taki þátt í API beiðninni.

Umfang þess *Reiknaðu Söluskjal* API er bara útreikningur á verði og afslætti. Skattar og gjöld koma ekki við sögu.

Eftirfarandi tafla sýnir inntaksfæribreytur inni í hlutnum sem er nefndur **söluskjal**.

| Nafn             | Undirnafn | Gerð | Áskilið/valfrjálst | Lýsing |
|------------------|----------|------|-------------------|-------------|
| Kenni               | | strengur | Áskilið | Auðkenni söluskjalsins. |
| CartLines        | | IList\<CartLine\> | Valfrjálst | Listi yfir línur til að reikna út verð og afslætti fyrir. |
|                  | Vörukenni | Langt | Nauðsynlegt í umfangi CartLine | Auðkenni vöruskráningar. |
|                  | ItemId | strengur | Valfrjálst | Auðkenni vörunnar. Ef gildi er gefið upp verður það að passa við gildið **Vöruauðkenni** breytu. |
|                  | InventoryDimensionId | strengur | Valfrjálst | Auðkenni birgðavíddar. Ef gildi er gefið upp, samsetningin af **ItemId** og **InventoryDimensionId** gildi verða að passa við gildi **Vöruauðkenni** breytu. |
|                  | Magn | aukastaf | Nauðsynlegt í umfangi CartLine | Magn vörunnar. |
|                  | UnitOfMeasureTákn | strengur | Valfrjálst | Eining vörunnar. Sjálfgefið, ef gildi er ekki gefið upp, notar API sölueiningu vörunnar. |
| CustomerId       | | strengur | Valfrjálst | Reikningsnúmer viðskiptavinarins. |
| Vildarkortaauðkenni    | | strengur | Valfrjálst | Auðkenni vildarkortsins. Sérhver viðskiptareikningur sem er tengdur vildarkortinu verður að passa við verðmæti **Skilríki viðskiptavinar** breytu (ef hún er til staðar). Vildarkortið verður ekki tekið til greina ef það finnst ekki eða staða þess er það **Lokað**. |
| AffiliationLines | | IList\<AffiliationLoyaltyTier\> | Valfrjálst | Sambandshollustulínur. Ef **Skilríki viðskiptavinar** og/eða **Vildarkortaauðkenni** gildi eru gefin upp, verða samsvarandi tryggðarflokkslínur tengdar sameinaðar línum sem eru gefnar upp í **AffiliationLines** gildi. |
|                  | AffiliationId | Langt | Áskilið innan umfangs AffiliationLoyalty Tier | Auðkenni tengslaskrárinnar. |
|                  | LoyaltyTierId | Langt | Áskilið innan umfangs AffiliationLoyalty Tier | Skráningarauðkenni vildarflokks. |
|                  | AffiliationTypeValue | int | Áskilið innan umfangs AffiliationLoyalty Tier | Gildi sem gefur til kynna hvort tengilínan sé af **Almennt** tegund (**0**) eða **Hollusta** tegund (**1**). Ef þessi færibreyta er stillt á **0**, API tekur **AffiliationId** gildi sem auðkenni og hunsar **LoyaltyTierId** gildi. Ef það er stillt á **1**, API tekur **LoyaltyTierId** gildi sem auðkenni og hunsar **AffiliationId** gildi. |
|                  | ReasonCodeLines | Innheimta\<ReasonCodeLine\> | Áskilið innan umfangs AffiliationLoyalty Tier | Ástæðukóðalínur. Þessi færibreyta hefur engin áhrif á útreikning verðlagningar en er nauðsynleg sem hluti af **AffiliationLoyalty Tier** mótmæla. |
|                  | CustomerId | strengur | Áskilið innan umfangs AffiliationLoyalty Tier | Reikningsnúmer viðskiptavinarins. |
| Afsláttarmiðar          | | IList\<Coupon\> | Valfrjálst | Afsláttarmiðar sem eiga ekki við (óvirkir, útrunnir eða fundust ekki) verða ekki teknir til greina í verðútreikningnum. |
|                  | Kóði | strengur | Nauðsynlegt í umfangi afsláttarmiða | Afsláttarmiðakóði. |
|                  | CodeId | strengur | Valfrjálst | Auðkenni afsláttarmiðakóða. Ef gildi er gefið upp verður það að passa við gildið **Kóði** breytu. |
|                  | Afsláttartilboðskenni | strengur | Valfrjálst | Afsláttarauðkenni. Ef gildi er gefið upp verður það að passa við gildið **Kóði** breytu. |

**Dæmi um beiðnir**

```json
{
    "salesDocument": 
    {
        "Id": "CalculateSalesDocument",
        "CartLines": 
        [
            {
                "ProductId": 68719491408,
                "ItemId": "91003",
                "InventoryDimensionId": "",
                "Quantity": 1,
                "UnitOfMeasureSymbol": "ea"
            },
            {
                "ProductId": 68719493014,
                "Quantity": 2,
                "UnitOfMeasureSymbol": "ea"
            }
        ],
        "CustomerId": "3003",
        "AffiliationLines": 
        [
            {
                "AffiliationId": 68719476742,
                "LoyaltyTierId": 0,
                "AffiliationTypeValue": 0,
                "ReasonCodeLines": [],
                "CustomerId": null
            }
        ],
        "LoyaltyCardId": "55103",
        "Coupons": 
        [
            {
                "CodeId": "CODE-0005",
                "Code": "CPN0004",
                "DiscountOfferId": "ST100077"
            }
        ]
    }
}
```

Öllum körfuhlutnum er skilað sem svarhluti. Til að athuga verð og afslætti ættir þú að einbeita þér að reitunum í eftirfarandi töflu.

| Nafn           | Undirnafn | Gerð | Lýsing |
|----------------|----------|------|--------------|
| Nettóverð       | | aukastaf | Nettóverð alls söluskjalsins áður en afslættir eru notaðir. |
| Afsláttarupphæð | | aukastaf | Heildarafsláttarupphæð alls söluskjalsins. |
| Heildarupphæð    | | aukastaf | Heildarupphæð alls söluskjalsins. |
| CartLines      | | IList\<CartLine\> | Reiknaðar línur sem innihalda upplýsingar um verð og afslátt. |
|                | Verð | aukastaf | Einingaverð vörunnar. |
|                | Nettóverð | aukastaf | Nettóverð línunnar áður en afslættir eru notaðir (=*Verð*&times;*Magn*). |
|                | Afsláttarupphæð | aukastaf | Afsláttarupphæðin. |
|                | Heildarupphæð | aukastaf | Endanleg heildarverðlagningarniðurstaða línunnar. |
|                | PriceLines | IList\<PriceLine\> | Verðupplýsingar, þar á meðal uppruna verðsins (grunnverð, verðleiðrétting eða viðskiptasamningur) og upphæð. |
|                | Afsláttarlínur | IList\<DiscountLine\> | Upplýsingar um afslátt. |

## <a name="getavailablepromotions"></a>GetAvailablePromotions 

Gefið körfu sem hefur nokkrar körfulínur, the *GetAvailablePromotions* API skilar öllum viðeigandi afslætti fyrir körfulínurnar. 

Helsta notkunartilvikið fyrir *GetAvailablePromotions* API er körfusíðan, þar sem smásalar vilja sýna fram á notaða afslætti eða tiltæka afsláttarmiða fyrir núverandi körfu.

Eftirfarandi tafla sýnir inntaksfæribreytur fyrir *GetAvailablePromotions* API.

| Nafn        | Gerð | Áskilið/valfrjálst | Lýsing |
|-------------|------|-------------------|-------------|
| lykill         | strengur | Áskilið | Auðkenni körfu. |
| cartLineIds | IEtalanlegur\<string\> | Valfrjálst | Stilltu þessa færibreytu til að skila aðeins afslætti fyrir valdar körfulínur. |

**Dæmi um svarhluti**

```json
{
    "value": 
    [
        {
            "LineId": "f495ffa507bc4f63a47a409cd8713dd7",
            "Promotion": {
                "OfferId": "ST100012",
                "OfferName": "Loyalty 5% off over $100",
                "PeriodicDiscountTypeValue": 4,
                "IsDiscountCodeRequired": false,
                "ValidationPeriodId": null,
                "AdditionalRestrictions": null,
                "Description": "All loyalty members get 5% with transaction total above $10 unless some exclusive or best price discounts are already applied on the transaction",
                "ValidFromDate": "2022-06-20T06:52:56.2460219Z",
                "ValidToDate": "2022-06-20T06:52:56.2460224Z",
                "CouponCodes": [],
                "ValidationPeriod": null
            }
        }
    ]
}
```

## <a name="addcoupons"></a>AddCoupons

The *AddCoupons* API styður að bæta lista yfir afsláttarmiða í körfu. Það skilar körfuhlutnum eftir að afsláttarmiðunum er bætt við.

Eftirfarandi tafla sýnir inntaksfæribreytur fyrir *AddCoupons* API.

| Nafn                 | Gerð | Áskilið/valfrjálst | Lýsing |
|----------------------|------|-------------------|-------------|
| lykill                  | strengur | Áskilið | Auðkenni körfu. |
| afsláttarmiðakóðar          | IEtalanlegur\<string\> | Áskilið | Afsláttarmiðakóðar til að bæta í körfuna. |
| isLegacyAfsláttarkóði | ból | Valfrjálst | Stilltu þessa færibreytu á **satt** til að gefa til kynna að afsláttarmiðinn sé eldri afsláttarkóði. Sjálfgefið gildi er **rangt**. |

## <a name="removecoupons"></a>Fjarlægja afsláttarmiða

The *Fjarlægja afsláttarmiða* API styður að fjarlægja lista yfir afsláttarmiða úr körfu. Það skilar körfuhlutnum eftir að afsláttarmiðar eru fjarlægðir.

Eftirfarandi tafla sýnir inntaksfæribreytur fyrir *Fjarlægja afsláttarmiða* API.

| Nafn        | Gerð | Áskilið/valfrjálst | Lýsing |
|-------------|------|-------------------|-------------|
| lykill         | strengur | Áskilið | Auðkenni körfu. |
| afsláttarmiðakóðar | IEtalanlegur\<string\> | Áskilið | Afsláttarmiðakóðar til að fjarlægja úr körfunni. |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
