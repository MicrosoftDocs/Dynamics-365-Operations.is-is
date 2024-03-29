---
title: Rangt reitargildi í TaxTrans
description: Í þessari grein er að finna upplýsingar um úrræðaleit á röngum reitargildum í TaxTrans.
author: EricWangChen
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 6e7329ffdc04207116c92cb42e02750b176713fc
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899815"
---
# <a name="incorrect-field-value-in-taxtrans"></a>Rangt reitargildi í TaxTrans

[!include [banner](../includes/banner.md)]

Ef reitgildi í **TaxTrans** er rangt skal nota upplýsingarnar í þessari grein til að reyna að leysa vandamálið.

## <a name="overview-of-values"></a>Yfirlit yfir gildi
Eftirfarandi listi sýnir hvernig **TaxTrans**, **TaxUncommitted** og **TmpTaxWorkTrans** eru svipuð gagnasett en virka öðruvísi.

  - **TaxTrans** er síðasta niðurstaða bókaðrar skattfærslu í gagnagrunninum.
  - **TaxUncommitted** er milliútreikningur á skattaniðurstöðu sem helst í gagnagrunninum (ef það á við), sem verður notaður síðar í bókun.
  - **TmpTaxWorkTrans** er tímabundin reiknuð skattútkoma í töflunni í minninu (Töflagerð = InMemory).

Ef þú finnur grunnorsök fyrir röngum dálki **TaxTrans** hefurðu einnig fundið grunnorsökina á röngum dálki **TaxUncommitted** og **TmpTaxWorkTrans**. Þetta er vegna þess að dálkarnir þrír eru afritaðir af hverjum öðrum.

Yfirleitt er **TmpTaxWorkTrans** búið til við skattaútreikning og síðan, er **TaxUncommitted** búið til, ef við á. Á meðan á skattafærslu stendur myndast **TaxTrans**.


## <a name="add-breakpoints"></a>Bæta við rofstöðum
Til að bæta við rofstöðum skal ljúka eftirfarandi skrefum: 

1. Bæta viðbótum og rofstöðum við í *insert()* og *update()* í viðbótunum eins og sýnt er hér að neðan.

     - **TaxTrans**

        ```x++
        [ExtensionOf(tableStr(TaxTrans))]
        public final class TaxTrans_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - **TaxUncommitted**

        ```x++
        [ExtensionOf(tableStr(TaxUncommitted))]
        public final class TaxUncommitted_Extension
        {
            public void insert()
            {
                next insert();
            }
        
            public void update()
            {
                next update();
            }
        
        }
        ```

     - **TmpTaxWorkTrans**

        ```x++
        [ExtensionOf(tableStr(TmpTaxWorkTrans))]
        public final class TmpTaxWorkTrans_Extension
        {
            public void insert(boolean _ignoreCalculatedSalesTax)
            {
                next insert(_ignoreCalculatedSalesTax);
            }
        
            public void update(boolean _ignoreCalculatedSalesTax)
            {
                next update(_ignoreCalculatedSalesTax);
            }
        
        }
        
        ```

2. Einnig er hægt að bæta við rofstöðum beint þegar **TaxUnCommitted** er ekki innifalið.

     - *TaxTrans.insert()*, *TaxTrans.update()*
     - *TmpTaxWorkTrans.insert()*, *TmpTaxWorkTrans.update()*

## <a name="reproduce-and-debug"></a>Endurgera og kemba

Eftir að rofpunktar hafa verið stilltir verða allar breytingar á varanleika gagna sýnilegar við kembun. Til að finna grundvallarorsök á röngum dálki **TaxTrans**, **TaxUncommitted** eða **TmpTaxWorkTrans** skal yfirfara og hafa eftirfarandi atriði í huga:

- Síðasti rofstaðurinn þar sem dálkurinn er réttur.
- Fyrsti rofstaður þar sem dálkurinn er rangur.
- Hvað gerist á milli þessara tveggja punkta.

## <a name="determine-whether-customization-exists"></a>Ákvarða hvort sérstilling sé til staðar
Ef þú hefur lokið við skrefin í fyrri hlutum en hefur ekki getað leyst vandamálið skaltu skoða hvort sérstillingar séu til staðar. Ef sérstilling er til staðar skal hafa samband við notendaþjónustu Microsoft til að fá aðstoð.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

