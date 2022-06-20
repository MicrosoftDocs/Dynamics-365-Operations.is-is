---
title: Uppsetning og viðhald samstarfs lánardrottna
description: Þessi grein útskýrir hvernig á að setja upp samstarf lánardrottna í Dynamics 365 Supply Chain Management. Þar er einnig útskýrt hvernig hægt er að úthluta nýjum notendum lánardrottnasamstarfs og stjórna öryggishlutverkum fyrir þessa notendur.
author: GalynaFedorova
ms.date: 12/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DirExternalRole, SysUserRequestListPage, VendVendorPortalUsers, WorkflowTableListPageRnr
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.custom: 220774
ms.assetid: 69d05e8b-7dc2-48ea-bc24-bea9ac963579
ms.search.region: Global
ms.author: gfedorova
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 8fe4731f8ff23f4abe25fce57a2325e1fca979c4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8890829"
---
# <a name="set-up-and-maintain-vendor-collaboration"></a>Uppsetning og viðhald samstarfs lánardrottna

[!include [banner](../includes/banner.md)]

Viðmót fyrir samstarf lánardrottna sýnir takmarkaðar upplýsingar um innkaupapantanir, reikninga og vörusendingabirgðir til ytri lánardrottna. Í þessu viðmóti getur lánardrottinn einnig svarað tilboðsbeiðnum og skoðað og breytt grunnupplýsingum um fyrirtækið.

Þessi grein útskýrir hvernig á að setja upp samstarf lánardrottna í Dynamics 365 Supply Chain Management. Þar er einnig útskýrt hvernig á að setja upp verkflæði til að úthluta nýjum notendum lánardrottnasamstarfs og stjórna öryggishlutverkum fyrir þessa notendur.

> [!NOTE]
> Upplýsingarnar um uppsetningu öryggishlutverka fyrir samstarf lánardrottna eiga aðeins við um núverandi útgáfu af Finance and Operations. Í Microsoft Dynamics AX 7.0 (febrúar 2016) og Microsoft Dynamics AX forritaútgáfu 7.0.1 (maí 2016) notarðu kerfiseininguna **Gátt lánardrottins** fyrir samskipti við lánardrottna. Upplýsingar um heimildir notanda fyrir lánardrottnagáttina í Microsoft Dynamics AX er að finna í [Öryggi notanda í gátt lánardrottins](configure-security-vendor-portal-users.md).

## <a name="set-up-vendor-collaboration-security-roles"></a>Setja upp öryggishlutverk lánardrottnasamstarfs

Starfsmaður innkaupa eða lánardrottinn sem er með nægar heimildir getur beðið um að tengiliður verði gerður að notanda með því að virkja **Úthluta lánardrottni** í færslu tengiliðar. Meðan á úthlutunarferlinu stendur eru heimildir notanda valdar fyrir nýja ytri notandann og ný beiðni lánardrottins er send inn. Mikilvægt er að þú setjir heimildir notanda rétt upp sem hægt er að velja í lánardrottnabeiðninni. Annars gætu lánardrottnar fengið aðgang að upplýsingum sem þeir eiga ekki að vera með aðgang að í Supply Chain Management.

### <a name="set-up-the-security-roles-that-are-available-for-selection-when-a-new-user-request-is-used-for-a-contact-person"></a>Setja upp öryggishlutverk sem hægt er að velja þegar ný notandabeiðni er notuð fyrir tengilið

1. Veldu **Kerfisstjórnun** &gt; **Öryggi** &gt; **Ytri hlutverk**.
2. Veldu **Nýtt** og veldu svo öryggishlutverk og hlutverkið **Lánardrottinn**.

Þú gætir viljað bæta við hlutverkunum **Stjórnandi lánardrottins (ytri)** og **Lánardrottinn (ytri)** sem eru gefin upp í Supply Chain Management. Einnig er hægt að nota öryggishlutverk sem fyrirtækið hefur búið til.

Þú ættir aðeins að bjóða upp á hlutverkið **Stjórnandi lánardrottins (ytri)** ef lánardrottnar eiga að geta búið til nýja tengiliði, senda inn notandabeiðnir lánardrottnasamstarfs fyrir nýja notendur og breytingar á upplýsingum notanda og meðhöndlað þessar beiðnir í gegnum verkflæði.

Ef ætlunin er að setja upp tengiliði lánardrottins og notendur er hægt að gera eingöngu **Hlutverk lánardrottins (ytri)** aðgengilegt. Þetta hlutverk verður þá eina hlutverkið sem hægt er að biðja um í gegnum notandabeiðni lánardrottins.

> [!NOTE]
> Hlutverkið **SystemUser** er veitt sjálfkrafa þegar þú stofnar nýjan lykil notanda handvirkt. Þess vegna verður að fjarlægja það hlutverk og úthluta hlutverkinu **SystemExternalUser**. Ef nýir notandareikningar eru stofnaðir í gegnum verkflæðið sem hefst á lánardrottnabeiðni um að úthluta nýjum notanda, verða eitt eða fleiri hlutverk sem hafa verið sett upp fyrir samstarf lánardrottins og hlutverkið **SystemExternalUser** úthlutuð.

#### <a name="vendor-admin-external-security-role"></a>Öryggishlutverk stjórnanda lánardrottins (ytri)

Hægt er að nota hlutverkið **Stjórnandi lánardrottins (ytri)** fyrir ytri lánardrottna sem vinna með tengiliðaupplýsingar lánardrottins og gera beiðnir um að úthluta nýjum notendum lánardrottnasamstarfs. Ytri notendur sem eru með þetta öryggishlutverk geta framkvæmt eftirfarandi verk:

- Skoðaðu og breyttu tengiliðaupplýsingum á borð við titil, netfang og símanúmer einstaklings.
- Bættu nýjum eða fyrirliggjandi tengilið við lánardrottnalykil sem þeir eru tengiliður fyrir.
- Eyða öllum tengiliðum sem þeir hafa búið til.
- Gerðu tengslin milli tengiliðar og lánardrottnalykils virk eða óvirk. Þegar tengslin milli tengiliðar og lánardrottnalykils eru óvirk er ekki hægt að vísa í tengilið í nýjum innkaupapöntunum eða öðrum skjölum.
- Hafnaðu eða leyfðu aðgang tengiliðar að skjölum í viðmóti lánardrottnasamstarfs sem tengjast lánardrottnalyklinum. Þegar tengslin milli tengiliðar og lánardrottnalykils eru gerð óvirk verður aðgangi að skjölum sem tengjast lánardrottnalyklinum alltaf hafnað.
- Óska eftir nýjum notandareikningi fyrir tengilið með því að nota aðgerðina **Úthluta notanda**.
- Óska eftir því að notandareikningur tengiliðar verði gerður óvirkur.
- Óska eftir því að notandareikningi tengiliðs sé breytt til að bæta við eða fjarlægja öryggishlutverk.
- Skoða tilboðsbeiðnir.

#### <a name="vendor-external-security-role"></a>Öryggishlutverk lánardrottins (ytri)

Hægt er að nota **Hlutverk lánardrottins (ytri)** fyrir ytri lánardrottna sem vinna með innkaupapantanir. Ytri notendur sem eru með þetta öryggishlutverk geta framkvæmt eftirfarandi verk:

- Svara og skoða upplýsingar um innkaupapantanir.
- Vinna með reikninga lánardrottna í samstarfi.
- Skoða vörusendingarbirgðir.
- Skoða og svara tilboðsbeiðnum.
- Skoða lánadrottnaupplýsingar.

## <a name="set-up-security-roles-that-are-used-when-prospective-vendors-are-onboarded"></a>Setja upp öryggishlutverk sem eru notuð þegar væntanlegir lánardrottnar eru teknir inn

Til að taka lánardrottna inn sem eru innleiddir í gegnum skráningarbeiðni væntanlegs lánardrottins, þarf að setja upp ytra öryggishlutverk. Þessu hlutverki verður úthlutað á nýja notendur í úthlutunarferlinu sem verkflæðið af gerðinni **Verkflæði notandabeiðni (verkvangur)** stýrir. Fyrir frekari upplýsingar, sjá [Settu upp verkflæði til að vinna úr notendabeiðnum um samvinnu lánardrottins](#set-up-workflows-to-process-vendor-collaboration-user-requests) kafla síðar í þessari grein.

Upplýsingar um hvernig hægt er að innleiða væntanlega lánardrottna er að finna í [Taka inn lánardrottna](vendor-onboarding.md).

### <a name="set-up-a-security-role-that-is-used-when-a-new-prospective-vendor-user-request-is-submitted"></a>Setja upp öryggishlutverk sem er notað þegar ný notandabeiðni væntanlegs lánardrottins er send inn

1. Veldu **Kerfisstjórnun** > **Öryggi** > **Ytri hlutverk**.
2. Veldu **Nýtt** og veldu svo öryggishlutverk og hlutverkið **Væntanlegur lánardrottinn**.

Þú ættir að bæta við hlutverkinu **Væntanlegur lánardrottinn (ytri)** sem er boðið upp á í Supply Chain Management.

Öryggishlutverkið veitir aðeins aðgang að leiðsagnarforriti fyrir skráningu á nýjum lánardrottni.

## <a name="set-up-workflows-to-process-vendor-collaboration-user-requests"></a>Setja upp verkflæði til að vinna úr notandabeiðni lánardrottnasamstarfs

Til að tryggja að öllum viðkomandi verkum sé lokið og að viðeigandi samþykki séu veitt þarf að setja upp verkflæði til að meðhöndla notandabeiðnir lánardrottnasamstarfs.

Notandabeiðnir lánardrottnasamstarfs eru sendar inn af annaðhvort ytri lánardrottnum sem eru með öryggishlutverkið **Stjórnandi lánardrottins (ytri)** eða svipuðum heimildum, eða starfsmanni innkaupa í fyrirtækinu þínu. Einnig er hægt að búa þær til úr skráningarbeiðnum væntanlegs lánardrottins í innleiðingarferli lánardrottins.

Til eru þrjár gerðir af beiðnum:

- Beiðnir um að úthluta nýjum notanda
- Beiðnir um að gera fyrirliggjandi notanda óvirkan
- Beiðnir um að breyta öryggishlutverkum fyrirliggjandi notanda

Frekari upplýsingar um notandabeiðnir lánardrottnasamstarfs er að finna í [Stjórna notendum fyrir samstarf lánardrottna](manage-vendor-collaboration-users.md).

Þú verður að búa til tvö eða fleiri verkflæði til að vinna úr öllum þremur gerðunum af notandabeiðnum lánardrottnasamstarfs. Ný verkflæði eru búin til á síðunni **Notendaverkflæði**.

### <a name="example-of-a-workflow-for-provisioning-new-users-and-modifying-security-roles"></a>Dæmi um verkflæði fyrir úthlutun nýrra notenda og breytingar á öryggishlutverkum

Til að meðhöndla lánardrottnabeiðnir til að búa til nýja notendur og breyta öryggishlutverkum er hægt að setja á skilyrði greinar við upphaf verkflæðisins. Þannig er notuð önnur grein verkflæðisins eftir því hvort beiðnin á að búa til nýjan notanda eða breyta notanda sem er til.

Til að setja upp þessa grein skal búa til nýtt verkflæði af gerðinni **Verkflæði notandabeiðni (verkvangur)**. Greinar verkflæðisins geta innihaldið eftirfarandi einingar.

#### <a name="branch-to-provision-new-users"></a>Grein til að úthluta nýjum notendum

1. Úthluta samþykktarverki á einstaklinginn sem ber ábyrgð á að samþykkja að nýir notendur eigi að fá aðgang að upplýsingum um lánardrottnasamstarfs.
2. Úthlutaðu verki á einstaklinginn sem ber ábyrgð á að biðja um nýjan notandareikning Microsoft Azure Active Directory (Azure AD) í Azure-gáttinni. Notaðu fyrirfram skilgreinda verkið **Senda B2B-notanda Azure boð** fyrir þetta skref. Hægt er að flytja B2B-notendur sjálfkrafa út í Azure AD. Notaðu fyrirframskilgreinda **Úthlutun Azure AD B2B-notanda**. Frekari upplýsingar er að finn aí [Flytja út B2B-notendur í Azure AD](../../fin-ops-core/dev-itpro/sysadmin/implement-b2b.md).
3. Úthlutaðu samþykktarverki á einstaklinginn sem hleður upp í Azure. Ef ekki tekst að stofna reikning hafnar þessi einstaklingur verkinu og endar verkflæðið. Hægt er að sleppa þessu samþykktarverki ef þú tókst með skrefið sem flytur sjálfkrafa út nýja notandareikninga í Azure í gegnum B2B-forritunarviðmótið.
4. Bættu sjálfvirku verki sem úthlutar nýjum notanda. Notaðu fyrirframskilgreinda verkið **Sjálfvirkur ráðstöfunarnotandi** fyrir þetta verk.
5. Bættu við verki sem lætur nýja notandann vita. Þú gætir viljað senda nýja notandanum kynningartölvupóst sem inniheldur vefslóð fyrir Supply Chain Management. Þessi tölvupóstur getur notað sniðmát sem þú býrð til á síðunni **Tölvupóstskeyti** og velur síðan á síðunni **Færibreytur notandaverkflæðis**. Sniðmátið getur innihaldið **%portalURL%** merkið. Þegar kynningartölvupósturinn er búinn til verður þessu merki skipt út fyrir vefslóð leigjanda Supply Chain Management.

    > [!NOTE]
    > Þetta verkflæði er hægt að nota í mörgum aðstæðum sem fela í sér innleiðingu notanda. Til dæmis er hægt að nota það þegar væntanlegir lánardrottnar eða tengiliðir þurfa reikning lánardrottnasamstarfs. Því ættir þú að orða tölvupóstinn sem almenna yfirlýsingu sem er hægt að nota í margvíslegum tilgangi.

#### <a name="branch-to-modify-security-roles"></a>Grein til að breyta öryggishlutverkum

1. Úthluta samþykktarverki á einstaklinginn sem ber ábyrgð á að samþykkja breytingar á öryggishlutverkum.
2. Bættu sjálfvirku verki sem bætir við eða fjarlægir viðkomandi öryggishlutverk. Notaðu verkið **Sjálfvirkur ráðstöfunarnotandi** fyrir þetta skref.

### <a name="example-of-a-workflow-for-inactivating-a-user"></a>Dæmi um verkflæði til að gera notanda óvirkan

Búa til verkflæði af gerðinni **Gera verkvang verkflæðis notandabeiðni óvirkan** og bættu svo við eftirfarandi verkum.

1. Úthlutaðu samþykktarverki á einstaklinginn sem ber ábyrgð á að samþykkja beiðnir um að gera notendur óvirka. Þú getur bætt við skilyrðum til að gera þetta samþykktarskref sjálfvirkt.
2. Bættu við sjálfvirku verki sem gerir notandann óvirkan. Notaðu verkið **Sjálfvirk óvirkjun notanda** fyrir þetta skref.
3. Bættu við hvaða hreinsunarverki sem þarf á að halda. Til dæmis er hægt að bæta við verki sem fjarlægir reikninginn úr skráasafninu í Azure-gáttinni.

## <a name="enable-vendor-collaboration-for-a-specific-vendor"></a>Virkja samstarf lánardrottna fyrir tiltekinn lánardrottin

Áður en þú stofnar notandareikning fyrir einhvern sem mun nota samstarf lánardrottna þarf að setja upp lánardrottin svo hann geti notað samstarf lánardrottna. Á síðunni **Lánardrottnar** á **Almennt** flipanum skal stilla **Virkja samstarf** svæðið. Eftirtaldir valkostir eru í boði:

- **Virk (Innkaupapöntun er staðfest sjálfkrafa)** – Innkaupapantanir eru sjálfkrafa staðfestar ef lánardrottinn samþykkir þær án þess að óska eftir breytingum.
- **Virk (Innkaupapöntun er ekki staðfest sjálfkrafa)** - Fyrirtækið þitt þarf að staðfesta innkaupapantanir handvirkt eftir að lánardrottinn hefur samþykkt þær.

> [!NOTE]
> Starfsmenn innkaupa í fyrirtækinu þínu geta einnig lokið verkinu.

## <a name="troubleshoot-the-provisioning-of-new-vendor-collaboration-users"></a>Úrræðaleita úthlutun nýrra notenda lánardrottnasamstarfs

Nýjum notendum lánardrottnasamstarfs er úthlutað í gegnum verkflæðið sem þú setur upp til að vinna úr notandabeiðnum lánardrottnasamstarfs af gerðinni **Úthlutun lánardrottins**.

Ef netfang nýs notanda lánardrottnasamstarfs tilheyrir léni sem skráð hjá Azure sem leigjandi (þ.e. ef það er stýrður lénsreikningur) verður netfangið að vera fyrirliggjandi Azure AD reikningur. Að öðrum kosti er ekki hægt að ljúka úthlutunarferlinu.

Frekari upplýsingar um ferlið sem notað er í verkinu **Senda boð til B2B-notanda Azure** í verkflæðinu fyrir stjórnun Azure AD reiknings er að finna í [Azure Active Directory B2B-samstarf](/azure/active-directory/external-identities/what-is-b2b).

## <a name="additional-resources"></a>Frekari upplýsingar

[Samstarf lánardrottna með ytri lánardrottnum](vendor-collaboration-work-external-vendors.md)

Horfðu á stutt myndband um innleiðingarferli lánardrottins: [Nýliðun nýrra lánardrottna](https://www.youtube.com/watch?v=0KUc3AGaTKk&feature=youtu.be)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
