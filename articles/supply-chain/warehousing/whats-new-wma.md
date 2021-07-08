---
title: Nýjungar eða breytingar í farsímaforriti Warehouse Management
description: Í þessu efnisatriði er að finna lista yfir nýja og breytta eiginleika fyrir hverja útgefna útgáfu af farsímaforriti Warehouse Management fyrir Microsoft Dynamics 365 Supply Chain Management.
author: ivanv-microsoft
ms.date: 06/07/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-07
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 61124728942c0b8162de9f687ae752773c47d07e
ms.sourcegitcommit: 4cbd83e21a78459e4711a2dedba0f5a7acc3c841
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/15/2021
ms.locfileid: "6261782"
---
# <a name="whats-new-or-changed-in-the-warehouse-management-mobile-app"></a>Nýjungar eða breytingar í farsímaforriti Warehouse Management

[!include [banner](../includes/banner.md)]

Í þessu efnisatriði er að finna nýja eiginleika, lagfæringar, endurbætur og þekkt vandamál fyrir hverja útgefna útgáfu af farsímaforriti Warehouse Management fyrir Microsoft Dynamics 365 Supply Chain Management.

## <a name="version-2060"></a>Útgáfa 2.0.6.0

### <a name="new-features-fixes-and-improvements-in-version-2060"></a>Nýir eiginleikar, lagfæringar og bætur í útgáfu 2.0.6.0

Þessi útgáfa kynnir eftirfarandi nýja eiginleika, lagfæringar og endurbætur:

- Sýnistilling sýnir nú öll merki á tungumáli tækis.
- Minni líkur eru á að fá eftirfarandi villuboð: „Ekki er hægt að finna hentugt yfirlit fyrir tilgreinda stærð.“
- Lágmarkshæð vinnuspjalds hefur verið aukin (í tilvikum þar sem þrír eða færri reitir eru stilltir á að birtast í verkefnalistanum).
- Spássíur neðst á upplýsingaspjöldum hafa verið endurbættar.
- Ógild tákn í XML-skrám sem skipst er á við þjóninn eru nú meðhöndluð á hnökralausan hátt. (Til dæmis eru stafir sem prentast ekki nú meðhöndlaðir á hnökralausan hátt og leiða ekki lengur til þess að forritið frjósi.)
- HTTP-villur (eins og „villa 503“) þegar netþjónsbeiðni er send er nú meðhöndlaðar á hnökralausan hátt.
- Þó að villa sé sýnd er listinn yfir valmöguleika ekki lengur sýndur sjálfkrafa fyrir stýringar samsettra glugga.
- Forritið frýs ekki lengur vegna skjástefnunar sem er valin í notandastillingum.
- Myndir afurða eru nú sýndar í sjálfsafgreiðsluumhverfum. (Þessi breyting á eingöngu við um útgáfur í lágri upplausn. Þjónusta skráarstjórnunar styður ekki myndir í fullri stærð í sjálfsafgreiðsluumhverfum.)
- Vandamál varðandi of litla tiltekt upp á núll í magni hefur verið lagað.
- Forritið frýs ekki lengur þegar upplýsingaspjald sýnir marga eins reiti.

### <a name="known-issues-in-version-2060"></a>Þekkt vandamál í útgáfu 2.0.6.0

Eftirfarandi þekkt vandamál eru til í þessari útgáfu:

- Með tímanum hægist á forritinu (sérstaklega verkefnalistanum).
- **Windows-útgáfa:** Þegar USB-skanni er notaður til að skanna í Windows valda ósamkvæmar niðurstöður því að skönnuð tákn blandast saman.

## <a name="version-2050"></a>Útgáfa 2.0.5.0

Þessi útgáfa kynnir eftirfarandi nýja eiginleika, lagfæringar og endurbætur:

- Leyniorð biðlara er ekki lengur falið í uppsetningu tengistillingarinnar.
- Nú er hægt að ýta lengi á hvaða texta sem er til að sjá hann til fulls.
- Villuboðin þegar vantar geymsluheimildir hafa verið endurbætt.
- Nýjum stýringarröðum hefur verið bætt við sum flæðin.
- Hnappur innsendingar verður ekki lengur í boði á röngum tímum vegna gluggastærðar.
- Sleðar geta nú verið áfram á smærri skjáum þegar stærri hnappastærðir eru notaðar.
- Fjögurra hnappa yfirlögnin er ekki lengur klippt burt.
- Lyklaborðið styður nú hnapp eyðingar.
- Leyst hefur verið úr birtuvandamáli sem gæti komið upp þegar ýtt er á lyklaborðið.
- Búið er að laga ýmis vandamál varðandi sýnigögn.
- Leyst hefur verið úr vandamáli sem hafði áhrif á talnareiti á upplýsingasíðunni.
- Skjályklaborðið hverfur ekki lengur af og til á sumum tækjum.
- Ýmsar villur í notendaviðmóti hafa verið lagfærðar, svo sem villur sem höfðu áhrif á bakgrunnslit og staðsetningu.
- Rússneska í viðmótinu hefur verið bætt.
- Ýmis vandamál sem ollu því að kerfið fraus hafa verið löguð.
- Leyst hefur verið úr vandamáli sem tengdist enduropnun reiknivélarinnar.
- **Android útgáfa:** Leyst hefur verið úr vandamáli sem leiddi til þess að Android 4.4 fraus við ræsingu.
- **Android útgáfa:** Lágmarksskölun hefur verið minnkuð um 50 prósent.

## <a name="version-2040"></a>Útgáfa 2.0.4.0

Útgáfa 2.0.4.0 var fyrsta almenna útgáfan sem var í boði í farsímaforriti Warehouse Management.

### <a name="new-features-fixes-and-improvements-in-version-2040"></a>Nýir eiginleikar, lagfæringar og bætur í útgáfu 2.0.4.0

Þessi útgáfa kynnir eftirfarandi nýja eiginleika, lagfæringar og endurbætur sem voru ekki í boði í forútgáfunni:

- Ef upplýsingaspjald inniheldur tvö merki sem eru með eins gögn verður eitt merkið falið.
- Sérstafir eru nú sjálfgefið sýndir og valkosturinn til að fela þá hefur verið fjarlægður úr notandastillingum.
- Óvirkir innsendingarhnappar eru nú sýndir ótiltækir í smækkuðu yfirliti.
- Breyting á rökum röðunar fyrir stýringar tryggja hnökralausa skölun milli tækja. Þar af leiðandi er minni þörf á að laga skölun leturgerða eða hnappa.
- Sjálfgefna litaþemanu hefur verið breytt í *Dökkt*.
- Táknið sem vantar fyrir óvirkan innsendingarhnapp hefur verið bætt við borðayfirlitið.
- Undanþágur vegna tímalokunar fara nú með notanda yfir á tengingarsíðuna í stað þess að sýna villu í línunni.
- Ef engin innsendingaraðgerð er í boði (t.d. **Í lagi**, **Já**, **Samþykkja**, **Búið** eða **Lokið**) verður innsendingarhnappurinn gerður óvirkur.
- Stöðugleiki forrits hefur verið bættur.
- Komin er lagfæring á veikleika öryggis [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).
- **Windows-útgáfa:** Vandamál í Windows þar sem valmyndir svöruðu ekki eftir að stærð glugga var breytt hefur verið lagað.

### <a name="known-issue-in-version-2040"></a>Þekkt vandamál í útgáfu 2.0.4.0

Eftirfarandi þekkt vandamál er til staðar í þessari útgáfu:

- Vandamál kom upp í þessari útgáfu með tæki sem notar Android 4.4. Þú gætir lent í vandamálum þegar forritið er notað í þessari Android-útgáfu.
