---
title: Store Commerce app fyrir farsímakerfi
description: Þessi grein lýsir því hvernig á að byrja að nota Microsoft Dynamics 365 Commerce Store Commerce app fyrir Android og iOS.
author: stuharg
ms.date: 10/07/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2018-10-29
ms.openlocfilehash: 1f07a130629863ebd9d036378436cf360e90ac26
ms.sourcegitcommit: 98231ff810f41f9fcdc6b536d87e453028aa6db8
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 10/07/2022
ms.locfileid: "9641681"
---
# <a name="store-commerce-app-for-mobile-platforms"></a>Store Commerce app fyrir farsímakerfi

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig á að byrja að nota Microsoft Dynamics 365 Commerce Store Commerce öpp fyrir Android og iOS.

The Dynamics 365 Commerce farsímaforrit fyrir Android og iOS gera ferlið við að setja upp fullkomin farsímasölustað (POS) tæki fyrir smásöluumhverfi þitt einfalt og einfalt. Store Commerce farsímaforritin bjóða upp á alla möguleika og kosti [Store Commerce app fyrir Windows](store-commerce.md) á formþáttum síma og spjaldtölva. Hægt er að setja upp Store Commerce farsímaforritin beint frá Apple og Google Play app verslunum og krefjast þess ekki að þróunaraðili búi til nýjan forritapakka til að dreifa eða uppfæra þau. 

Store Commerce farsímaforritin halda fullum virknijafnvægi við núverandi blendingaöpp smásölu. Að auki inniheldur Store Commerce fyrir iOS stuðning fyrir sérstaka vélbúnaðarstöð, þannig að iOS tæki geta átt samskipti við nettengdar greiðslustöðvar, kvittunarprentara og peningaskúffur án þess að þurfa að nota sameiginlega vélbúnaðarstöð. 

> [!IMPORTANT]
> Store Commerce öppin fyrir Windows,Android, og iOS eru næsta kynslóð POS forrita fyrir Dynamics 365 Commerce. Núverandi Modern POS (MPOS) forritið og [Smásala blendingsforrit](hybridapp.md) fyrir farsíma verður úrelt í október 2023. Microsoft mælir með því að þú notir Store Commerce eða Cloud POS (CPOS) fyrir allar nýjar POS uppsetningar. Núverandi viðskiptavinir ættu að ætla að flytja úr Retail hybrid appinu yfir í Store Commerce. Fyrir frekari upplýsingar um afskriftaáætlun fyrir MPOS og Retail blendingsforritin, sjá [Nútímavæða Dynamics 365 Commerce tæknistafla í verslun](https://www.microsoft.com/download/details.aspx?id=103896). 

## <a name="app-architecture"></a>App arkitektúr

Store Commerce farsímaforritin nota sömu staðfræði og Store Commerce appið fyrir Windows þegar það er notað í blendingham. Store Commerce farsímaforritin eru skelforrit sem gera CPOS beint frá Commerce Scale Unit (CSU) og tengjast höfuðstöðvum Headless Commerce og Commerce í gegnum CSU. Skeljaforritslíkanið gerir Store Commerce forritum kleift að styðja sérstaka vélbúnaðarstöð fyrir beina samþættingu við greiðslustöð, prentara, peningaskúffu og önnur jaðartæki. Þú þarft ekki að setja upp sameiginlega vélbúnaðarstöð til að nota vélbúnaðartæki. 

Til að uppfæra Store Commerce farsímaforrit skaltu bara uppfæra CSU. Öll ný POS virkni og eiginleikar verða sjálfkrafa sóttir af appinu. Fyrir frekari upplýsingar um hvernig á að uppfæra CSU, sjá [Notaðu uppfærslur og viðbætur á Commerce Scale Unit (ský)](../../fin-ops-core/dev-itpro/deployment/update-retail-channel.md).

Skeljaröppin eru þjónustað í gegnum uppfærslur á appverslun. Þegar minni útgáfa nær almennu framboði (GA) mun Microsoft birta hana í appaverslunum. Microsoft gæti einnig birt plástra á milli minniháttar útgáfuuppfærslur til að gefa út forgangs villuleiðréttingar.

## <a name="prerequisites"></a>Forkröfur

Store Commerce farsímaforritin krefjast Dynamics 365 Commerce, sérstaklega höfuðstöðvar viðskipta og CSU hluti. Eftirfarandi tafla sýnir lágmarksútgáfur stýrikerfis (OS) og CSU sem krafist er af Android og iOS farsímaforrit. 

| Skilyrði | Android      | iOS  |
| ------------ | ------------ | ---- |
| Útgáfa stýrikerfis   | 7.0          | 15,0 |
| CSU útgáfa  | 9,38,22266,8 | Tilkynnt síðar  |

## <a name="install-the-app"></a>Setja upp forritið

Þú getur sett upp Store Commerce farsímaforrit beint úr Google Play versluninni eða Apple App Store. 

- [Store Commerce app fyrir Android](https://aka.ms/storecommerceandroid)
- Store Commerce app fyrir iOS (fáanlegt fljótlega)

The Android app (.apk) og Apple app (.ipa) pakka er einnig hægt að hlaða niður úr Samnýtt eignasafni í Microsoft Dynamics Lífsferilsþjónusta. 

## <a name="device-and-register-setup"></a>Uppsetning tækis og skráningar

Áður en hægt er að virkja skrá í farsímaöppum Store Commerce verður þú að setja upp tæki og skrá í höfuðstöðvum Commerce. Fyrir frekari upplýsingar, sjá [Tæki og skrár](../implementation-considerations-devices.md). 

### <a name="device-setup"></a>Uppsetning tækis

Til að búa til og setja upp nýtt tæki skaltu fylgja þessum skrefum.

1. Í höfuðstöðvum viðskipta, farðu til **Verslun og verslun \> Rásaruppsetning \> POS uppsetning \> Tæki**. 
1. Búðu til nýtt tæki og veldu annað hvort **Nútíma POS -Android** eða **Nútíma POS - iOS** sem forritategund, allt eftir farsímaforritinu sem þú ert að nota. 

    > [!NOTE] 
    > The **Nútíma POS -Android** og **Nútíma POS - iOS** forritagerðir eru einnig notaðar til að dreifa núverandi tvinnforritum fyrir Android og iOS. Eftir úreldingu MPOS verða merkingar fyrir þessar forritagerðir uppfærðar í **Verslun -Android** og **Nútíma POS - iOS**. 

### <a name="register-setup"></a>Uppsetning afgreiðslukassa

Þú getur búið til nýja skrá og tengt hana við tækið sem þú bjóst til, eða þú getur tengt núverandi skrá við nýja tækið þitt. Fyrir frekari upplýsingar um skrár, sjá [Búa til og tengja skrár](../tasks/create-associate-registers.md).

### <a name="screen-layout-setup"></a>Uppsetning skjás

Ef þú ert að endurnýta skjáskipulag sem er innifalið í kynningargögnunum sem fylgja með Dynamics 365 Commerce leyfi, Store Commerce appið velur sjálfkrafa meðfylgjandi samsett skipulag ef skjáupplausn tækisins þíns er minni en 480&times; 853 pixlar í andlitsmynd. Hins vegar, ef þú ert að búa til skjáuppsetningu frá grunni, eða ef farsíminn þinn notar stærri upplausn en þétta útlitið styður, vertu viss um að búa til upplausn og tilheyrandi hnappatöflur sem henta símanum eða spjaldtölvunni sem þú ætlar að dreifa til. Fyrir frekari upplýsingar um stillingar skjáskipulags, sjá [POS notendaviðmót sjónrænar stillingar](../pos-screen-layouts.md). 

Eftir að tæki og skrár hafa verið stillt, í höfuðstöðvum Commerce, farðu á **Verslun og verslun \> Auðkenni verslunar og viðskipta \> Dreifingaráætlanir**, og keyrðu skráningarverkið.

## <a name="activate-a-device"></a>Virkjaðu tæki

Til að virkja tæki á Store Commerce farsímaforriti skaltu fylgja þessum skrefum.

1. Opnaðu appið á farsímanum.
1. Sláðu inn CPOS vefslóðina, sem þú getur fundið á umhverfisupplýsingasíðunni í Lifecycle Services, eða á **Rásarsnið** síða í höfuðstöðvum viðskipta (**Verslun og verslun \> Rásaruppsetning \> Rásarsnið**).
1. Skráðu þig inn með því að nota skilríki starfsmanns sem hefur leyfi til að stjórna tækjum.
1. Veldu verslunina sem tengist skránni sem þú bjóst til eða endurnotaðir í höfuðstöðvum Commerce.
1. Veldu skrána sem þú tengdir við tækið sem þú bjóst til í höfuðstöðvum Commerce.
1. Nú ætti tækið þitt að vera virkjað. Þú getur skráð þig inn á skrána með því að nota símanúmer og lykilorð fyrir starfsmann sem er tengdur við verslunina sem þú valdir. 

Fyrir frekari upplýsingar um virkjun tækis, sjá [Virkjun á sölustað (POS) tæki](retail-device-activation.md#activate-a-modern-pos-or-cloud-pos-device-by-using-guided-activation).

## <a name="feature-parity-with-store-commerce-for-windows"></a>Eiginleikajafnvægi við Store Commerce fyrir Windows

Eftirfarandi tafla ber saman getu Store Commerce appsins yfir Windows,Android, og iOS palla.

| Eiginleiki                                                                               | Windows | Android | iOS |
| ------------------------------------------------------------------------------------- | ------- | ------- | --- |
| Sérhæfð vélbúnaðarstöð                                                            | Já     | Já     | Já |
| Sameiginleg vélbúnaðarstöð                                                               | Já     | Já     | Já |
| Samskipti við nettengt jaðartæki (greiðslustöð, prentara og peningaskúffu) | Já     | Já     | Já |
| OLE for Point of Sale (OPOS) jaðartæki í gegnum staðbundna vélbúnaðarstöð             | Já     | Nr.      | Nr.  |
| Ótengdur hamur                                                                          | Já     | Nr.      | Nr.  |

## <a name="additional-resources"></a>Frekari upplýsingar

[Store Commerce-forrit](store-commerce.md)

[Veldu á milli Store Commerce og sölukerfis í skýinu](../mpos-or-cpos.md)

[Leysa uppsetningu og uppsetningarvandamál í Store Commerce](../troubleshoot/store-commerce-setup-installation.md)
