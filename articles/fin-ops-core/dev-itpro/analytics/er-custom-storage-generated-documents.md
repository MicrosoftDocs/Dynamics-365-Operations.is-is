---
title: Tilgreina sérsniðinn geymslustað fyrir skjöl sem eru mynduð
description: Þessi grein útskýrir hvernig á að stækka listann yfir geymslustaði fyrir skjöl sem snið rafrænnar skýrslugerðar myndar.
author: kfend
ms.date: 02/22/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: 10
ms.openlocfilehash: 83ee74cf590fe559ae18161d68b38dff54ab7fbc
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/12/2022
ms.locfileid: "9268756"
---
# <a name="specify-a-custom-storage-location-for-generated-documents"></a>Tilgreina sérsniðinn geymslustað fyrir skjöl sem eru mynduð

[!include[banner](../includes/banner.md)]

Forritunarviðmót forritsins (API) fyrir ramma rafrænnar skýrslugerðar gerir þér kleift að stækka listann yfir geymslustaði fyrir skjöl sem snið rafrænnar skýrslugerðar myndar. Í þessari grein er að finna yfirlit aðalverkefnanna sem þarf að klára til að bæta við sérsniðnum geymslustað.

## <a name="prerequisites"></a>Forkröfur

Þú verður að setja upp grannfræði sem styður samfellda smíði. (Nánari upplýsingar er að finna í [Setja upp grannfræði sem styður samfellda smíði og sjálfvirkni prófunar](/dynamics365/unified-operations/dev-itpro/perf-test/continuous-build-test-automation).) Þú verður að hafa aðgang að þessari grannfræði fyrir eitt af eftirfarandi hlutverkum:

- Þróunaraðili rafrænnar skýrslulausnar
- Hagnýtur ráðgjafi vegna rafrænnar skýrslugerðar
- Kerfisstjóri

Þú verður einnig að hafa aðgang að þróunarumhverfi fyrir þessa grannfræði.

## <a name="create-or-import-an-er-format-configuration"></a>Búa til eða flytja inn skilgreiningu fyrir snið rafrænnar skýrslugerðar

Í núverandi grannfræði, [stofnarðu nýtt snið rafrænnar skýrslugerðar](tasks/er-format-configuration-2016-11.md) til að mynda skjöl sem áformað er að bæta við sérsniðinn geymslustað. Annars [flytja núverandi snið rafrænnar skýrslugerðar inn í þessa grannfræði](general-electronic-reporting-manage-configuration-lifecycle.md).

![Síða sniðshönnuðar.](media/er-extend-file-storages-format.png)

> [!IMPORTANT]
> Snið rafrænnar skýrslugerðar sem þú býrð til eða flytur inn verður að innihalda að minnsta kosti eina af eftirfarandi sniðseiningum:
>
> - Skrá
> - Mappa
> - Samruni
> - Viðhengi

## <a name="create-a-new-document-type"></a>Stofna nýja gerð skjala

Til að tilgreina hvernig skjöl eru send sem snið rafrænnar skýrslugerðar myndar er nauðsynlegt að skilgreina [Viðtökustaðir rafrænnar skýrslugerðar (ER)](electronic-reporting-destinations.md). Í sérhverjum viðtökustað rafrænnar skýrslugerðar sem er skilgreindur til að geyma mynduð skjöl sem skrár, þarf að tilgreina gerð skjals fyrir skjalastjórnunarramma. Mismunandi skjalagerðir er hægt að nota til að senda skjöl sem mismunandi snið rafrænnar skýrslugerðar mynda.

1. Bæta við nýrri [skjalagerð](../../fin-ops/organization-administration/configure-document-management.md) fyrir snið rafrænnar skýrslugerðar sem þú bjóst til eða fluttir inn áður. Í skýringarmyndinni sem fylgir er skjalagerðin **FileX**.
2. Til að aðgreina þessa skjalategund frá öðrum skjalategundum skal hafa með tiltekið lykilorð í heitinu. Til dæmis, í skýringarmyndinni sem fylgir er heitið **(LOCAL) mappa**.
3. Í reitnum **Klasi** skal tilgreina **Hengja skrá við**.
4. Í reitnum **Flokkur** skal tilgreina **Skrá**.

![Síða skjalagerðar.](media/er-extend-file-storages-document-type.png)

> [!NOTE]
> Gerðir skjala miðast við fyrirtæki. Til að nota snið rafrænnar skýrslugerðar með skilgreindum viðtökustað í mörgum fyrirtækjum verður að skilgreina aðskilda gerð skjals í hverju fyrirtæki fyrir sig.

## <a name="review-source-code"></a>Yfirfara frumkóða

Yfirfara kóða aðferðarinnar **insertFile()** af klasanum **ERDocuManagement**. Takið eftir að tilvikið **AttachingFile()** kemur upp á meðan myndaða skráin er hengd við færslu.


```xpp
/// <summary>
/// Inserts file as attachment in Document Management.
/// </summary>
/// <param name = "_owner">A record as the attachment owner.</param>
/// <param name = "_stream">The file stream.</param>
/// <param name = "_filePath">The file path with name.</param>
/// <param name = "_attachmentName">The name of file attachment.</param>
/// <returns>The reference to inserted file.</returns>
[Hookable(false)]
public DocuRef insertFile(
    Common _owner, 
    System.IO.Stream _stream, 
    str _filePath, 
    str _attachmentName, 
    DocuTypeId _docuTypeId)
{
    DocuRef docuRef;
    if (_stream)
    {
        DocuType::createDefaults();
        if (!this.isDocuTypeValid(_docuTypeId))
        {
            throw error(strFmt("@ElectronicReporting:DocuTypeIsNotValid", _docuTypeId));
        }
        var args = ERDocuManagementAttachingFileEventArgs::construct(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        ERDocuManagementEvents::onAttachingFile(args);
        if (args.isHandled())
        {
            docuRef = args.getDocuRef();
        }
        else
        {
            docuRef = this.attachFile(_owner, _stream, _filePath, _attachmentName, _docuTypeId);
        }
    }
    return docuRef;
}
```

Tilvikið **AttachingFile()** kemur upp þegar unnið er úr eftirfarandi viðtökustöðum rafrænnar skýrslugerðar:

- **Safnvista** - Þegar þessi viðtökustaður er notaður er búin til ný færsla í töflunni ERFormatMappingRunJobTable fyrir það snið rafrænnar skýrslugerðar sem er keyrt. Svæðið **Safnvistað** í þessari færslu er stillt á **Ósatt**. Ef keyrsla á sniði rafrænnar skýrslugerðar tekst er myndaða skjalið hengt við þessa færslu og tilvikið **AttachingFile()** kemur upp. Gerð skjals sem er valið í þessum viðtökustað rafrænnar skýrslugerðar ákvarðar geymslustaðinn fyrir viðhengda skrá (Microsoft Azure Geymsla eða Microsoft SharePoint mappa).
- **Safnvistun vinnslu** - Þegar þessi viðtökustaður er notaður er búin til ný færsla í töflunni ERFormatMappingRunJobTable fyrir það snið rafrænnar skýrslugerðar sem er keyrt. Svæðið **Safnvistað** í þessari færslu er stillt á **Satt**. Ef keyrsla á sniði rafrænnar skýrslugerðar tekst er myndaða skjalið hengt við þessa færslu og tilvikið **AttachingFile()** kemur upp. Gerð skjals sem er skilgreind í færibreytum rafrænnar skýrslugerðar ákvarðar geymslustaðinn fyrir viðhengda skrá (Azure-geymsla eða SharePoint mappa).

![Færibreytusíða rafrænnar skýrslugerðar.](media/er-extend-file-storages-parameters.png)

## <a name="configure-an-er-destination"></a>Skilgreina viðtökustað rafrænnar skýrslugerðar

1. Skilgreina safnvistaðan viðtökustað fyrir einn af áðurnefndum þáttum (skrá, mappa, samruni eða viðhengi) í sniði rafrænnar skýrslugerðar sem var búinn til eða fluttur inn. Til leiðbeiningar skal sjá [Viðtökustaðir rafrænnar skýrslugerðar](/dynamics365/unified-operations/dev-itpro/analytics/tasks/er-destinations-2016-11).
2. Notaðu gerð skjals sem þú bættir við á undan fyrir skilgreindan viðtökustað. (Fyrir dæmið í þessari grein er gerð skjals **FileX**.)

![Svargluggi áfangastaðastillinga.](media/er-extend-file-storages-destination.png)

## <a name="modify-source-code"></a>Breyta frumkóða

1. Bæta nýjum klasa við Microsoft Visual Studio verkið og skrifa kóða til að gerast áskrifandi að tilvikinu **AttachingFile()** sem var minnst á hér á undan. (Nánari upplýsingar um mynstur stækkunarhæfni sem er notað skal sjá [Svara með því að nota EventHandlerResult](/dynamics365/unified-operations/dev-itpro/extensibility/respond-event-handler-result).) Til dæmis, í nýja klasanum, skrifa kóða sem framkvæmir eftirfarandi aðgerðir:

    1. Geymið myndaðar skrár í möppu staðbundins skráakerfis á þjóninum sem keyrir AOS-þjónustu.
    2. Geymið aðeins þessar mynduðu skrár þegar nýja skjalagerðin (til dæmis gerðin **FileX** sem er með lykilorðið „(LOCAL)“ í heitinu) er notuð þegar skrá er hengd við færsluna í kladda fyrir vinnsluverk rafrænnar skýrslugerðar.

    ```xpp
    class ERDocuSubscriptionSample
    {
        void new()
        {
        }
        [SubscribesTo(classStr(ERDocuManagementEvents), 
        staticDelegateStr(ERDocuManagementEvents, 
        attachingFile))]
        public static void ERDocuManagementEvents_attachingFile(ERDocuManagementAttachingFileEventArgs _args)
        {
            if (!_args.isHandled())
            {
                DocuType docuType = DocuType::find(_args.getDocuTypeId());
                if (strContains(docuType.Name, '(LOCAL)'))
                {
                    _args.markAsHandled();
                    var stream = _args.getStream();
                    if (stream.CanSeek)
                    {
                        stream.Seek(0, System.IO.SeekOrigin::Begin);
                    }
                    using (var localStream = System.IO.File::OpenWrite(@'c:\0\' + _args.getAttachmentName()))
                    {
                        stream.CopyTo(localStream);
                    }
                }
            }
        }
    }
    ```

2. Endursmíðaðu verkefnið þitt.

## <a name="run-the-er-format-that-you-created-or-imported"></a>Keyra snið rafrænnar skýrslugerðar var búið til eða flutt inn

1. Framkvæma snið rafrænnar skýrslugerðar sem var búið til eða flutt inn.
2. Farðu í **Fyrirtækisstjórnun \> Rafræn skýrslugerð \> Vinnslur rafrænnar skýrslugerðar**. Finndu skrána sem var búin til fyrir þetta vinnsluverk, og sem hefur myndaða skrá sem viðhengi.
3. Kannaðu staðbundna **C:\\0** möppu til að finna sömu mynduðu skrá.

## <a name="additional-resources"></a>Frekari upplýsingar

- [Áfangastaðir rafrænnar skýrslugerðar (ER)](electronic-reporting-destinations.md)
- [Heimasíða stækkunarhæfni](../extensibility/extensibility-home-page.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
