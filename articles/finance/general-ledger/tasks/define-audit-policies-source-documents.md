---
title: Skilgreina endurskoðunarstefnur fyrir upprunaskjöl
description: Þetta efni útskýrir hvernig á að setja upp og keyra reglur endurskoðunarstefnu.
author: ryansandness
manager: AnnBe
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicySourceDocumentRuleType, SysFieldLookUp, SysPolicyListPage, SysPolicy, AuditPolicyRule, SysQueryForm, SysQueryFieldLookUp, AuditPolicyDateSelection, AuditPolicyAdditionalOption, BatchJob, CaseDetail
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba720fd1bbbbf8b4f3b936d65d9d7840432f291a
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 10/13/2020
ms.locfileid: "4444462"
---
# <a name="define-audit-policies-for-source-documents"></a>Skilgreina endurskoðunarstefnur fyrir upprunaskjöl

[!include [banner](../../includes/banner.md)]

Þetta efni útskýrir hvernig á að setja upp og keyra reglur endurskoðunarstefnu. Dæmi notar kostnaðarskýrslur með hótel kostnaðargerð. Þessi aðferð notar sýnigögn USMF fyrirtækisins. Endurskoðandahlutverkið inniheldur réttar heimildir til að framkvæma þessi verk.

1. Í skoðunarrúðunni ferðu í **Einingar > Vinnusvæði endurskoðunar > Uppsetning > Stefnureglugerð**.
2. Veljið **Nýtt**.
3. Í reitinn **Heiti reglu** skal slá inn gildi.
4. Í reitinn **Lýsing** skal slá inn gildi.
5. Í reitnum **Heiti fyrirspurnar** velurðu **Kostnaðarskýrslulínu**
6. í reitnum **Gerð fyrirspurnar** skal velja **Samanlagt**
7. Í reitnum **Lögaðili** skal velja **Lögaðila**
8. Í reitnum **Tilvísun í dagsetningu skjals** velurðu **Breytt dagsetning og tími**
9. Veljið **Vista**.
10. Í skoðunarrúðunni ferðu í **Einingar > Vinnusvæði endurskoðunar > Uppsetning > Endurskoðunarstefnur**.
11. Veljið **Nýtt**.
12. Í reitinn **Heiti** skal slá inn gildi.
13. Útvíkkaðu kaflann **Fyrirtækjaregla**.
14. Veljið **Contoso Entertainment System USA** í trénu og síðan **Bæta við**.
15. Veljið **Contoso Consulting USA** í trénu og síðan **Bæta við**.
16. Veljið **Contoso Retail USA** í trénu og síðan **Bæta við**.
17. Minnkaðu hlutann **Fyrirtækjaregla**.
18. Útvíkkaðu hlutann **Stefnuregla**.
19. Finna og velja síðan Stefnuregluna sem var stofnuð áður, á listanum.
20. Veldu **stefnureglu**.
21. Í retinum **Gildisdagsetningu** færirðu inn dagsetningu og tíma.
22. Velja **Síu**.
23. Á listanum skal velja línuna fyrir **Kostnaðartegund** og stilla upplýsingarnar á **Hótel**.
24. Í reitinn **Skilyrði** skal slá inn eða velja gildi.
25. Veldu flipann **Samanlagt**.
26. Veljið **Bæta við**.
27. Á listanum velurðu reitagildi sem er **Færsluupphæð**.
28. Í reitinn **Reitur** skal slá inn eða veldu gildi.
29. Í reitnum **AggregateFunction** velurðu **Samtölu**.
30. Veldu flipann **Flokka eftir**.
31. Veljið **Bæta við**.
32. Á listanum velurðu gildi fyrir **Starfsmann**.
33. Veljið **Bæta við**.
34. Á listanum velurðu gildi fyrir **Kostnaðartegund**.
35. Í reitinn **Reitur** skal slá inn eða veldu gildi.
36. Velja flipann **Með**.
37. Veljið **Bæta við**.
38. Veldu **Færsluupphæð**.
39. Í reitinn **Reitur** skal slá inn eða veldu gildi.
40. Í reitnum **AggregateFunction** velurðu **Samtölu**.
41. Í svæðinu **Skilyrði** skaltu færa inn `>2000`.
42. Veljið **Í lagi**.
43. Veldu **Prófa**.
44. Í reitnum **Upphafsdagsetning skjalavals** skaltu færa inn dagsetningu og tíma.
45. Í reitnum **Lokadagsetning skjalavals** skal færa inn dagsetningu og tíma.
46. Veldu **Keyra prófun**.
47. Á Aðgerðasvæðinu skal velja **Endurskoðunarstefnu**.
48. Veldu **Aukavalkosti**.
49. Í reitinn **Upphafsdagsetning** skal færa inn dagsetningu og tíma.
50. Í reitinn **Lokadagsetning** skal færa inn dagsetningu og tíma.
51. Veldu **Runu**.
52. Stækkaðu hlutann **Keyra í bakgrunni**.
53. Veldu **Já** í reitnum **Runuvinnsla**.
54. Veljið **Í lagi**.
55. Í skoðunarrúðunni ferðu í **Einingar > Vinnusvæði endurskoðunar > Endurskoða mál**.
56. Í listanum skal finna og velja þá skráningu sem óskað er eftir.
57. Útvíkkaður hlutann **Tengingar**.
58. Í listanum skal finna og velja þá skráningu sem óskað er eftir.

