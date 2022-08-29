---
title: Undirritaðu MPOS .appx skrána með kóða undirritunarskírteini
description: Þessi grein útskýrir hvernig á að undirrita MPOS með kóða undirritunarskírteini.
author: josaw1
ms.date: 05/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-09-2019
ms.custom: 28021
ms.openlocfilehash: bcf558b4b375078ed24777417e92b1c852f4c0eb
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282807"
---
# <a name="sign-the-mpos-appx-file-with-a-code-signing-certificate"></a>Undirritaðu MPOS .appx skrána með kóða undirritunarskírteini

[!include [banner](../includes/banner.md)]

Til að setja upp Modern POS (MPOS) verður þú að undirrita MPOS appið með kóða undirritunarskírteini frá traustum veitanda og setja upp sama vottorð á öllum vélunum þar sem MPOS er sett upp undir traustri rótarmöppu fyrir núverandi notanda.

Til að undirrita MPOS appið með vottorði skaltu nota einn af þessum valkostum í **Smásölu SDK\\ Byggja tól\\ Customization.settings** skrá:

- Bættu við öryggisskráarverkefni hlutanum af Azure DevOps byggja skref og hlaða upp vottorðinu til að tryggja skráarverkefnið. Notaðu breytu fyrir úttaksslóð öruggrar skráarverks sem færibreytu í Customization.settings skránni.

    > [!NOTE]
    > Örugg skrá verkefni styður ekki lykilorðsvarið vottorð. Þú verður að fjarlægja lykilorðið áður en þú hleður þessu verkefni upp. Vegna þess að vottorðinu er hlaðið upp í örugga skráarkerfisverkefnið í Azure, geturðu aðeins fjarlægt lykilorðið fyrir þetta skref. Hins vegar ættir þú að ræða það við öryggissérfræðinga þína um að fjarlægja lykilorðið til að ákvarða hvort þetta sé rétta aðgerðin fyrir verkefnið þitt. Ekki fjarlægja lykilorð vottorðsins fyrir aðrar aðstæður.
- Notaðu vottorð sem er í skráarkerfinu. Til að gera þetta skaltu hlaða niður eða búa til vottorð og setja það í skráarkerfið þar sem smíðin er í gangi. Umboðsmaður eða smíðanotandi sem hýst er af Microsoft ætti að hafa aðgang að þessari slóð og skrá.
- Notaðu þumalfingur til að fletta upp í skírteininu í versluninni og skráðu þig inn með því skírteini.

## <a name="use-a-secure-file-task-for-universal-windows-platform-app-signing"></a>Notaðu Secure File verkefni fyrir Universal Windows Platform app undirskrift

> [!NOTE]
> Þú getur líka notað Azure Key Vault til að geyma skírteinið og notað Azure sign tólið til að undirrita Modern POS .appx skrána og sjálfsafgreiðsluuppsetningar. Fyrir sýnishorn af leiðsluforskriftum og frekari upplýsingar, sjá [Settu upp byggingarleiðslu í Azure DevOps til að búa til smásölu sjálfsafgreiðslupakka](build-pipeline.md#set-up-a-build-pipeline-in-azure-devops-to-generate-retail-self-service-packages).

Notkun öryggisskrárverkefnis er ráðlögð aðferð við undirritun á Universal Windows Platform (UWP) app. Fyrir frekari upplýsingar um undirritun pakka, sjá [Stilltu undirritun pakka](/windows/uwp/packaging/auto-build-package-uwp-apps#configure-package-signing). Þetta ferli er sýnt á eftirfarandi mynd.

![MPOS app undirritunarflæði.](media/POSSigningFlow.png)

> [!NOTE]
> Eins og er styður OOB umbúðirnar aðeins undirritun á .appx skránni, mismunandi sjálfsafgreiðsluuppsetningar eins og MPOIS, RSSU og HWS eru ekki undirrituð af þessu ferli. Þú þarft að undirrita það handvirkt með SignTool eða öðrum undirritunarverkfærum. Vottorðið sem notað er til að undirrita .appx skrána verður að vera uppsett í vélinni þar sem Modern POS er uppsett.

## <a name="steps-to-configure-the-certificate-for-signing-in-azure-pipelines"></a>Skref til að stilla vottorðið fyrir innskráningu í Azure Pipelines

### <a name="certificate-in-the-file-systemsecure-location"></a>Vottorð í skráarkerfinu/öruggri staðsetningu

Sækja [Sækja skrá verkefni](/visualstudio/msbuild/downloadfile-task) og bæta því við sem fyrsta skrefið í byggingarferlinu. Kosturinn við að nota Secure File verkefnið er að skráin er dulkóðuð og sett á diskinn meðan á smíði stendur, sama hvort byggingaleiðslan heppnast, mistekst eða er hætt við. Skránni er eytt af niðurhalsstaðnum eftir að byggingarferlinu er lokið.

1. Sæktu og bættu við Secure File verkefninu sem fyrsta skrefið í Azure-byggingarleiðslunni. Þú getur hlaðið niður öryggisskráarverkefninu frá [Hlaða niður skrá](https://marketplace.visualstudio.com/items?itemName=automagically.DownloadFile).
1. Hladdu upp vottorðinu í Secure File verkefnið og stilltu tilvísunarnafnið undir Output Variables, eins og sýnt er á eftirfarandi mynd.
    > [!div class="mx-imgBorder"]
    > ![Öruggt skráarverkefni.](media/SecureFile.png)
1. Búðu til nýja breytu í Azure Pipelines með því að velja **Ný breyta** undir **Breytur** flipa.
1. Gefðu upp heiti fyrir breytuna í gildisreitnum, til dæmis, **MySigningCert**.
1. Vistaðu breytuna.
1. Opnaðu **Customization.settings** skrá frá **RetailSDK\\ Byggingarverkfæri** og uppfærðu **ModernPOSPackageCertificateKeyFile** með breytuheitinu sem búið var til í leiðslunni (skref 3). Dæmi:

    ```Xml
    <ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(MySigningCert)</ModernPOSPackageCertificateKeyFile>
    ```
    Þetta skref er nauðsynlegt ef vottorðið er ekki varið með lykilorði. Ef vottorðið er varið með lykilorði skaltu halda áfram með eftirfarandi skrefum.
    
1. Ef þú vilt tímastimpla MPOS .appx skrána þegar þú undirritar hana með vottorði skaltu opna **Smásölu SDK\\ Byggja tól\\ Customization.settings** skrá og uppfæra **ModernPOSPackageCertificateTimestamp** breyta með tímastimplaveitunni (til dæmis,`http://timestamp.digicert.com`).
1. Á leiðslunni **Breytur** flipa, bættu við nýrri öruggri textabreytu. Stilltu nafnið á **MySigningCert.secret** og stilltu gildi lykilorðsins fyrir vottorðið. Veldu læsingartáknið til að tryggja breytuna.
1. Bæta við a **Powershell Script** verkefni í leiðsluna (eftir niðurhalið örugga skrá og fyrir smíða skrefið). Gefðu upp **Skjár** heiti og stilltu Tegund sem **Í línu**. Afritaðu og límdu eftirfarandi inn í handritshlutann.

    ```powershell
    Write-Host "Start adding the PFX file to the certificate store."
    $pfxpath = '$(MySigningCert.secureFilePath)'
    $secureString = ConvertTo-SecureString "$(MySigningCert.secret)" -AsPlainText -Force
    Import-PfxCertificate -FilePath $pfxpath -CertStoreLocation Cert:\CurrentUser\My -Password $secureString
    ```

1. Opnaðu **Customization.settings** skrá frá **RetailSDK\\ Byggingarverkfæri** og uppfærðu **ModernPOSPackageCertificateThumbprint** með þumalfingursgildi vottorðsins.

    ```Xml
       <ModernPOSPackageCertificateThumbprint Condition="'$(ModernPOSPackageCertificateThumbprint)' == ''"></ModernPOSPackageCertificateThumbprint>
    ```
 
Fyrir upplýsingar um hvernig á að fá þumalfingur fyrir vottorð, sjá [sækja þumalfingur skírteinis](/dotnet/framework/wcf/feature-details/how-to-retrieve-the-thumbprint-of-a-certificate#to-retrieve-a-certificates-thumbprint). 

## <a name="download-or-generate-a-certificate-to-sign-the-mpos-app-manually-using-msbuild-in-sdk"></a>Sæktu eða búðu til vottorð til að undirrita MPOS appið handvirkt með því að nota msbuild í SDK

Ef niðurhalað eða búið til vottorð er notað til að undirrita MPOS appið, þá er uppfærsla **ModernPOSPackageCertificateKeyFile** hnút í **Byggingarverkfæri\\ Customization.settings** skrá til að benda á pfx skráarstaðsetningu (**$(SdkReferencesPath)\\ appxsignkey.pfx**). Dæmi:

```xml
<ModernPOSPackageCertificateKeyFile Condition="'$(ModernPOSPackageCertificateKeyFile)' ==''">$(SdkReferencesPath)\appxsignkey.pfx</ModernPOSPackageCertificateKeyFile>
```

Í þessu tilviki er nafn skírteinisskrárinnar **appxsignkey.pfx**, staðsett í **Smásölu SDK\\ Tilvísun** möppu.

## <a name="use-thumbprint-to-sign-the-mpos-app"></a>Notaðu þumalfingur til að skrifa undir MPOS appið

Ef þú notar þumalfingur til að undirrita MPOS appið skaltu setja upp vottorðið á staðnum. Uppfærðu þumalputtagildið í **ModernPOSPackageCertificateThumbprint** hnút í **Byggingarverkfæri\\ Customization.settings** skrá.

Þessi valkostur mun virka ef smíðanotandinn er staðbundinn notandi. Hins vegar ef þú ert að nota Azure DevOps umboðsmenn til að búa til smíðina, þá gæti umboðsmaðurinn ekki fengið aðgang að vottunarversluninni til að nota skírteinið til undirritunar eða smíðavélin mun ekki hafa vottorðið uppsett. Í þessu tilviki er lausnin að breyta byggingarnotandanum í staðbundinn notanda og setja upp vottorðið í kassanum. Hins vegar mun þessi valkostur ekki virka ef þú hefur ekki stjórnandaaðgang að kassanum.

> [!NOTE]
> Ef .pfx skrá eða Örugg skrá verkefni valkostur er notaður til að undirrita forritið, farðu síðan úr **ModernPOSPackageCertificateThumbprint** hnút inn **Customization.settings** tómt. Ef þumalfingursvalkosturinn er notaður, farðu þá **ModernPOSPackageCertificateKeyFile** tómt. Ef bæði gildin eru uppfærð mun byggingin mistakast.

### <a name="certification-renewal"></a>Endurnýjun vottunar

### <a name="renew-a-certificate-from-trusted-ca"></a>Endurnýjaðu vottorð frá traustum CA

Hafðu samband við vottunaryfirvaldið þitt (CA) fyrir endurnýjunarferlið vottorðs. Fyrir traust vottorð er ekki krafist aðgerða á MPOS hliðinni.

### <a name="renew-a-self-signed-certificate"></a>Endurnýjaðu sjálfstætt undirritað vottorð

Ekki nota sýnishornsvottorðið sem er til í Retail SDK fyrir framleiðslu. Það er aðeins hægt að nota í þróunarskyni. Ekki er hægt að endurnýja sýnishorn Contoso vottorðsins og sýnishornsvottorðið sem fylgir Retail SDK útgáfu 10.0.16 eða eldri mun renna út 31. desember 2020. Ef þetta skírteini, eða sjálfundirritað vottorð, hefur verið notað til að undirrita sérsniðna nútíma POS, eru miklar líkur á að nútíma POS muni ekki virka rétt eftir þessa dagsetningu.
 
### <a name="impact"></a>Áhrif
 
Ef ofangreint er satt fyrir þig er vandamálið sem þú munt lenda í því að uppsetningarforritið mun ekki geta keyrt eftir 31. desember 2020. Það fer eftir upplýsingatæknistefnu fyrirtækisins sem notuð er, Modern POS gæti ekki virkað. Það er mikilvægt að þú prófir þetta með því að breyta dagsetningunni tímabundið í framtíðardagsetningu til að ákvarða áhrifin á fyrirtækið þitt.
 
### <a name="steps-to-determine-the-issue"></a>Skref til að ákvarða málið
 
1.  Notaðu Windows stillingar til að breyta tölvuklukkunni í dagsetningu og tíma árið 2021.
2.  Staðfestu að hægt sé að opna Modern POS, innskráningu geti átt sér stað og hægt sé að ljúka viðskiptum.
3.  Staðfestu að hægt sé að keyra Modern POS Self-service uppsetningarforrit og ef svo er mun sú uppsetning ljúka með góðum árangri.
4.  Settu Windows klukkustillingarnar aftur á rétta dagsetningu og tíma.
 
Ef þú getur klárað öll þessi skref án vandræða, þá muntu geta starfað á núverandi skírteini eftir 31. desember 2020.  
 
### <a name="steps-going-forward"></a>Skref fram á við 

Það er mjög mælt með því að þú endurnýjar áður notaða vottorðið. Við mælum eindregið með því að þú fáir nýtt skírteini. Til að gera þetta verður þú að framkvæma eina af eftirfarandi aðgerðum:
 
- **Æskilegt** - Fáðu kóða undirritunarvottorð frá traustum vottorðayfirvöldum.

- **Ekki valinn** - Búðu til sjálfundirritað kóða undirritunarvottorð til að nota. Þetta er venjulega aðeins notað í þróunarskyni innan léns og er ekki mælt með því fyrir framleiðslu. 

- **Í boði sem tímabundin lausn** - Notaðu endurnýjað Contoso kóða undirritunarvottorð. Þetta er venjulega notað í prófunarskyni, svo það er ekki mælt með því að það sé notað í framleiðslu.
 
Næst skaltu búa til nýjan sérsniðinn Modern POS pakka sem er undirritaður með því að nota þetta vottorð sem fæst með einni af aðgerðunum hér að ofan. Það fer eftir vottorðinu, eitt af eftirfarandi skrefum verður að fylgja:
 
- Ef þú notar nýtt, traust vottorð (eða nýtt, sjálfundirritað vottorð) verður þú að setja upp nýtt vottorð á hverju tæki. Eftir það þarftu að taka nýstofnaðan Modern POS pakkann (uppsetningarforrit), fjarlægja núverandi forrit og setja síðan upp nýja Modern POS pakkann aftur. Þú þarft að framkvæma tækisvirkjun á Modern POS á hverju tæki.

- Ef þú notar endurnýjað Contoso vottorð verður þú að setja upp nýja vottorðið á hverju tæki og setja upp Modern POS pakkann (uppsetningarforrit). Þú þarft ekki að fjarlægja, en þú verður að setja upp aftur á tækinu. Athugaðu að ekki verður krafist virkjunar á Modern POS. Þessi valkostur er tímabundin lausn. Notaðu aðeins þennan valkost til að forðast endurvirkjun og leysa málið áður en þú færð nýtt traust vottorð.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
