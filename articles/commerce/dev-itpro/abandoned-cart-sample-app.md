---
title: Greina yfirgefnar körfur og senda tilkynningar til viðskiptavina
description: Þessi grein lýsir því hvernig á að sérsníða Microsoft Dynamics 365 Commerce sýnishornsapp fyrir forláta körfutengi til að greina yfirgefnar kerrur og senda áminningar í tölvupósti til viðskiptavina.
author: bicyclingfool
ms.date: 02/25/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: stuharg
ms.search.validFrom: 2017-06-20
ms.openlocfilehash: 707640ca211e997533d0f5a0b4e6d52cb5be9db4
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8899211"
---
# <a name="detect-abandoned-carts-and-send-notifications-to-customers"></a>Greina yfirgefnar körfur og senda tilkynningar til viðskiptavina

[!include [banner](../includes/banner.md)]

Þessi grein lýsir því hvernig á að sérsníða Microsoft Dynamics 365 Commerce sýnishornsapp fyrir forláta körfutengi til að greina yfirgefnar kerrur og senda áminningar í tölvupósti til viðskiptavina.

Getan til að endurheimta tekjur og halda viðskiptavinum með tilkynningum um yfirgefin körfu er mikilvægur hæfileiki sem Dynamics 365 Commerce styður. Með því að sérsníða sýnishornsappið fyrir tengi fyrir Commerce yfirgefin körfu geta smásalar fengið aðgang að innkaupakörfum á Retail Server sem hefur ekki verið breytt á tímaglugga sem smásalarnir skilgreina. Þessar kerrur er síðan hægt að sækja, auka með vöru- og viðskiptavinagögnum og senda þeim til þriðja aðila markaðssetningaraðila í tölvupósti sem getur búið til tölvupósttilkynningar og sent þeim viðskiptavinum.

Tölvupósttilkynningin um yfirgefin körfu sem viðskiptavinir fá getur innihaldið eftirfarandi upplýsingar:

- Fornafn viðskiptavinarins.
- Eftirnafn viðskiptavinarins.
- Netfang viðskiptavinarins.
- Vefslóð sem skilar viðskiptavininum í körfuna sína.
- Viðskiptagjaldmiðillinn.
- Listi yfir vörur í körfu viðskiptavinarins. Fyrir hverja vöru eru eftirfarandi upplýsingar innifaldar:

    - Sýningarheiti vörunnar
    - Vöruauðkenni (notað til að setja saman vefslóð á vörulýsingasíðuna)
    - Vörumynd sem hægt er að breyta stærð sjálfkrafa til að mæta mismunandi stærðum útsýnisins
    - Alt texti fyrir vörumyndina
    - Einingaverð vörunnar

## <a name="abandoned-cart-connector-sample"></a>Sýnishorn af tengi fyrir körfu

Tengilíkan sem Microsoft útvegar í gegnum smásöluhugbúnaðarþróunarbúnaðinn (SDK) gerir kleift að sækja upplýsingar um yfirgefnar körfu og senda til þriðja aðila markaðssetningarþjónustu fyrir tölvupóst. Þetta tengi sér um samskipti við Retail Server, notar Azure Key Vault til öryggis, sér um tímasetningu á endurheimt körfu fyrir tiltekinn tíma og sækir pöntunar- og vörugögn. Það veitir einnig sýnishorn af útfærslu fyrir samþættingu við þriðja aðila markaðssetningaraðila fyrir tölvupóst. Tengið er byggt til að hafa samskipti við [Emarsys](https://emarsys.com) út fyrir kassann. Hins vegar er auðvelt að aðlaga það til að samþætta við aðrar lausnir, eins og Constant Contact, Mailchimp og SendGrid.

Eftirfarandi mynd sýnir íhluti sýnishornsforritsins fyrir yfirgefin körfutengi.

![Íhlutir sýnishornsforritsins fyrir yfirgefin körfutengi](media/AbandonedCartConnector.png)

> [!IMPORTANT]
> Sum svæði krefjast þess að viðskiptavinir geti afþakkað að fá gögn um körfu send til markaðsþjónustuaðila í tölvupósti eða beðið um að gögn þeirra verði fjarlægð. Hins vegar býður Microsoft ekki upp á þessa valkosti fyrir viðskiptavini. Þess vegna, ef þú ætlar að stunda viðskipti á svæðum sem bjóða þeim umboð, verður þú að útvega nauðsynlega innviði og sérstillingar til að fylgjast með óskum viðskiptavina og, byggt á þeim, koma í veg fyrir að gögn viðskiptavina berist á tölvupóstvettvanginn þinn. Þú verður einnig að skilgreina ferli til að hreinsa gögn viðskiptavina frá þjónustuveitunni fyrir markaðssetningu tölvupósts að beiðni viðskiptavinarins.

## <a name="obtain-the-code-sample"></a>Fáðu kóðasýnishornið

Forritið fyrir sýnishorn af körfutengi er innifalið í Retail SDK frá og með útgáfu 10.0.16. Kóðann má finna undir **\\ RetailSDK\\ Kóði\\ SampleExtensions\\ RetailServer\\ Viðbætur.AbandonedCartSample**. Fyrir frekari upplýsingar um Retail SDK og hvar það er hægt að nálgast það, sjá [Smásöluhugbúnaðarþróunarsett (SDK)](retail-sdk/retail-sdk-overview.md).

> [!NOTE]
> Þótt sýnishornskóðinn hafi fyrst verið gerður aðgengilegur í útgáfu 10.0.16, þá er hann samhæfur við útgáfu 10.0.13 og síðari smíði Retail Server.

## <a name="prerequisites-and-dependencies"></a>Forsendur og ósjálfstæði

Áður en hægt er að nota og stilla sýnishornskóðann fyrir yfirgefin körfutengi verður að uppfylla eftirfarandi forsendur.

### <a name="access-to-commerce-resources"></a>Aðgangur að viðskiptaauðlindum

Til að stilla og dreifa forláta körfutengiforritinu verður þú að hafa aðgang að eftirfarandi viðskiptaauðlindum:

- Aðgangur stjórnanda að höfuðstöðvum Commerce fyrir umhverfið þitt
- Aðgangur að Microsoft Dynamics Lifecycle Services (LCS) verkefni fyrir umhverfið þitt

### <a name="azure-cosmos-db"></a>Azure Cosmos DB

Forritið fyrir yfirgefin körfutengi notar Azure Cosmos DB til að rekja auðkenni og tímastimpla kerra sem áður hafa verið sóttar. Þú getur notað Azure Cosmos DB til að viðhalda þessum gögnum, eða þú getur sérsniðið kóðasýnishornið til að samþætta öðrum gagnageymslumöguleika. Fyrir frekari upplýsingar um Azure Cosmos DB, sjá [Velkomin til Azure Cosmos DB](/azure/cosmos-db/introduction).

Ef þú notar Azure Cosmos DB, eftirfarandi forsendur verða að vera uppfylltar áður en þú getur keyrt sýnishornið:

- Þú verður að hafa virkt Azure Cosmos DB reikning. Ef þú ert ekki með reikning, sjáðu [Búðu til gagnagrunnsreikning](/azure/cosmos-db/create-sql-api-dotnet#create-a-database-account).
- Þú verður að sækja **URI** og **AÐALLYKILL** (eða **ATVINNALYKILL**) gildi frá **Lyklar** blað Azure þinnar Cosmos DB reikning í Azure gáttinni. Fyrir frekari upplýsingar um hvernig á að sækja endapunkt og lykilupplýsingar fyrir Azure þinn Cosmos DB reikning, sjá [Skoðaðu, afritaðu og endurskapaðu aðgangslykla og lykilorð](/azure/cosmos-db/manage-account#keys).

### <a name="azure-key-vault"></a>Azure-lyklageymsla

Forritið fyrir yfirgefin körfutengi notar Key Vault til að geyma nöfn og leyndarmál mismunandi íhluta sem krefjast öruggs aðgangs.

Til að setja upp lyklageymslu skaltu fylgja þessum skrefum.

1. Fylgdu leiðbeiningunum í [Stjórnaðu Key Vault í Azure Stack Hub með því að nota gáttina](/azure-stack/user/azure-stack-key-vault-manage-portal?view=azs-2002&preserve-view=true).
2. Búðu til leyndarmál fyrir eftirfarandi upplýsingar:

    - Emarsys forritunarviðmót (API) notendanafn og API leyndarmál
    - Auðkenni og leyndarmál yfirgefin körfuforrit

Dæmiskóði fyrir yfirgefin körfutengi notar sjálfgefna Azure skilríki til að fá aðgang að Key Vault. Þú verður að veita **Listi** og **Lesið** heimildir fyrir auðkenninu sem þú ætlar að nota til að fá aðgang að Key Vault.

Fyrir frekari upplýsingar um sjálfgefna Azure skilríki, sjá [DefaultAzureCredential Class](/dotnet/api/azure.identity.defaultazurecredential?view=azure-dotnet&preserve-view=true).

## <a name="create-an-abandoned-cart-connector-sample-app-application-id-for-the-azure-ad-tenant"></a>Búðu til sýnishorn af forritaauðkenni fyrir körfutengi fyrir Azure AD leigjanda

Þú verður að búa til auðkenni forritaforrits fyrir yfirgefin körfutengi fyrir Azure Active Directory (AD) leigjanda. Fyrir upplýsingar um hvernig á að búa til forritsauðkenni, sjá [Notaðu gáttina til að búa til Azure AD umsóknar- og þjónustustjóri sem hefur aðgang að auðlindum](/azure/active-directory/develop/howto-create-service-principal-portal).

## <a name="add-the-abandoned-cart-connector-sample-app-application-id-to-the-allow-list-for-the-retail-server-api"></a>Bættu auðkenni forritaforrits fyrir forláta körfutengi við leyfislistann fyrir Retail Server API

Næst verður þú að bæta auðkenni forritaforrits fyrir yfirgefin körfutengi við leyfislistann fyrir smásöluþjóna API. Fyrir upplýsingar um hvernig á að bæta forritaauðkenni við leyfislistann í Azure, sjá [Stuðningur við þjónustu til þjónustu auðkenningar í smásöluþjóni](https://community.dynamics.com/ax/b/axforretail/posts/support-for-service-to-service-authentication-in-retail-server).

## <a name="configure-the-abandoned-cart-connector-sample-app"></a>Stilltu sýnishornsforritið fyrir yfirgefin körfutengi

Til að stilla sýnishornaforritið fyrir yfirgefin körfutengi skaltu breyta **appSettings.json** stillingarskrá sem er staðsett í rótinni á **AbandonedCartDetectionSample** Skrá. Eftirfarandi töflur lýsa eiginleikum stillingarskrár.

### <a name="keyvaultoptions"></a>KeyVaultOptions

| Eiginleiki    | Lýsing |
| ----------- | ----------- |
| KeyVaultURI | Domain Name System (DNS) nafn lykilhólfsins sem þú ert að nota í Azure gáttinni. |

### <a name="retailserverclientoptions"></a>RetailServerClientOptions

| Eiginleiki                                      | Lýsing |
| --------------------------------------------- | ----------- |
| TenantId                                      | The Azure AD leigjanda auðkenni Azure leigjanda þíns. |
| RetailServerAudienceId                        | Áhorfendaauðkenni smásöluþjónsins. Þú getur skilið eftir sjálfgefið gildi. |
| AppIdKeyVaultSecretName                       | Heiti leyndarmálsins sem þú bjóst til fyrir forláta körfutengi sýnishorn forritaforrits. |
| AppSecretKeyVaultSecretName                   | Nafn leyndarmálsins sem geymir forritsleyndarmálið fyrir yfirgefin körfutengi sýnishorn appauðkennis. |
| RetailServerUrl                               | Vefslóð smásöluþjónsins þíns. Þú getur fundið þetta gildi í LCS. |
| OperatingUnitNumber                           | Númer rekstrareiningar (OUN). Þú getur fundið þetta gildi í höfuðstöðvum Commerce. |
| Hafa yfirgefnar kerrurBreyttar síðan á síðustu mínútu | Upphaf tímagluggans fyrir yfirgefnu kerrurnar sem þú vilt sækja. Gildið er gefið upp sem nokkrum mínútum fyrir núverandi tíma. Til dæmis, stilltu þennan eiginleika á **120** til að sækja allar kerrur sem síðast var breytt fyrir 120 mínútum til loka tímagluggans sem er skilgreindur af **ÚtilokaAbandoned CartsModifiedSinceLastMinutes** eign. |
| ÚtilokaAbandoned CartsModifiedSinceLastMinutes | Lok tímagluggans fyrir yfirgefnu kerrurnar sem þú vilt sækja. Gildið er gefið upp sem nokkrum mínútum fyrir núverandi tíma. Til dæmis, ef **Hafa yfirgefnar kerrurBreyttar síðan á síðustu mínútu** eign er stillt á **120**, stilltu þennan eiginleika á **30** til að sækja allar kerrur sem voru breyttar fyrir 120 mínútum og fyrir 30 mínútum. Í reynd skilgreinir þessi eiginleiki þann tíma sem þú vilt bíða áður en körfu er lýst yfirgefin. |
| ReturnToCartUrl                               | Vefslóð körfunnar á netverslunarsíðunni þinni, á því sniði sem er notað í **app.config** skrá. |

### <a name="azurecosmosoptions"></a>AzureCosmosOptions

Staða yfirgefin körfuöflunarstarfs, auðkenni körfu og breyttir tímastimplar eru geymdir í Azure Cosmos DB. Sjálfgefið er að stillingarnar í stillingarskránni benda á staðbundið keppinautatilvik Azure Cosmos DB. Þegar þú setur tengið í framleiðslu verður þú að uppfæra þessar stillingar þannig að þær bendi á Azure Cosmos DB dæmi í Azure áskriftinni þinni. Fyrir staðbundnar eða sandkassaprófanir geturðu notað [Azure Cosmos DB Hermir](/azure/cosmos-db/local-emulator).

| Eiginleiki    | Lýsing |
| ----------- | ----------- |
| EndPointUri | Endpoint URI sem er veitt af Azure eða keppinautnum. |
| Aðallykill  | Aðallykillinn sem er útvegaður af Azure eða keppinautnum. |
| DatabaseId  | Auðkenni gagnagrunnsins. Þú getur skilið eftir sjálfgefið gildi eða gefið upp þitt eigið. |
| ContainerId | Gámaauðkennið. Þú getur skilið eftir sjálfgefið gildi eða gefið upp þitt eigið. |

### <a name="emarsysclientoptions"></a>EmarsysClientOptions

> [!NOTE]
> Ef þú ert að samþætta við annan markaðsaðila tölvupósts en Emarsys, verður þú að framlengja **IEmailProvider** tengi eftir því sem við á til að eiga samskipti við þann þjónustuaðila.

| Eiginleiki                      | Lýsing |
| ----------------------------- | ----------- |
| ApiUrl                        | `https://api.emarsys.net/api/v2/event/{0}/trigger` |
| ExternalEventId               | Auðkenni ytri atburðaskráningar sem er búin til í Emarsys. Þú getur fundið gildið undir **Kveikjastillingar** í herferðinni sem þú bjóst til til að senda tölvupósttilkynningar um yfirgefin körfu. |
| ApiUserNameKeyVaultSecretName | Nafn lykilsins þar sem Emarsys API notendanafnið er geymt. |
| ApiSecretKeyVaultSecretName   | Heiti lykilsins þar sem Emarsys API leyndarmálið er geymt. |
| EmarsysContactKeyId           | Auðkenni tölvupóstsdálksins í Emarsys tengiliðagagnagrunninum. Sjálfgefið gildi er **3** og ætti ekki að þurfa að breyta. |

### <a name="mediaoptions"></a>MediaOptions

Ef þú ert að nota rafræn viðskipti í Commerce geturðu notað stafræna eignastýringu Commerce til að sækja vörumyndir. Fyrir frekari upplýsingar um myndbreytingarmöguleika í stafrænni eignastýringu, sjá [Myndstillingar útsýnisstillingar](../e-commerce-extensibility/image-component.md#imagesettings-viewport-configuration).

| Eiginleiki                             | Lýsing |
| ------------------------------------ | ----------- |
| ImageServerUrl                       | Rótarslóð stafrænna eignaumsjónarmanns vefsvæðisins þíns. Þú getur fundið verðmæti í **Media Server Base URL** eignarlykill kl **Verslun og verslun \> Rásaruppsetning \> Rásarsnið** í höfuðstöðvum viðskipta. |
| ImageViewPorts                       | Gámahnúturinn fyrir einstakar útsýnisstillingar. |
| ImageViewPorts/viewport              | Útsýnisskilgreiningin. Notaðu þennan eiginleika til að tilgreina breiddarsvið fyrir útsýnisgluggann, í punktum. Fyrir dæmi sem sýnir hvernig þessi eign er notuð, sjáðu **appSettings.json** stillingarskrá. |
| ImageViewPorts/imageWidth            | Myndbreidd útsýnisins, í pixlum. |
| imageViewPorts/imageHeight           | Myndhæð útsýnisgluggans, í punktum. |
| imageViewPorts/useForDefaultImageTag | A **satt**/**rangt** gildi sem gefur til kynna hvort nota eigi myndstærðirnar sem eru skilgreindar af útsýnisglugganum ef`<picture>` HTML merki er ekki stutt fyrir vafra eða tölvupóstforrit. |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
