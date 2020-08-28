---
title: Uppsetning skjalaleiðar fyrir merkimiða á númeraplötu
description: Þetta efni lýsir því hvernig nota á sniðsaðferðir til að prenta gildi á merkimiða.
author: perlynne
manager: tfehr
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: ca7bf50800f3b376b809d89c5de969b2233c5e2b
ms.sourcegitcommit: d25d0feb3f8a5a760eba50ba5f46e1db02737d25
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 08/10/2020
ms.locfileid: "3677387"
---
# <a name="document-routing-layout-for-license-plate-labels"></a><span data-ttu-id="9600c-103">Uppsetning skjalaleiðar fyrir merkimiða á númeraplötu</span><span class="sxs-lookup"><span data-stu-id="9600c-103">Document routing layout for license plate labels</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9600c-104">Uppsetning skjalaleiðar skilgreinir uppsetningu á merkimiðum númeraplötu og gögnin sem eru prentuð á þá.</span><span class="sxs-lookup"><span data-stu-id="9600c-104">The document routing layout defines the layout of license plate labels, and the data that is printed on them.</span></span> <span data-ttu-id="9600c-105">Þú stillir prentunarkveikipunkta þegar þú setur upp valmyndaratriði farsíma og vinnusniðmát.</span><span class="sxs-lookup"><span data-stu-id="9600c-105">You configure the printing trigger points when you set up mobile device menu items and work templates.</span></span>

<span data-ttu-id="9600c-106">Í dæmigerðri atburðarás prenta starfsmenn í móttöku vöruhúsa merkimiða strax eftir að þeir skrá innihald bretta sem berast á móttökusvæðið.</span><span class="sxs-lookup"><span data-stu-id="9600c-106">In a typical scenario, warehouse receiving clerks print license plate labels immediately after they record the contents of pallets that arrive in the receiving area.</span></span> <span data-ttu-id="9600c-107">Efnislegir merkimiðar eru settir á brettin.</span><span class="sxs-lookup"><span data-stu-id="9600c-107">The physical labels are applied to the pallets.</span></span> <span data-ttu-id="9600c-108">Síðan er hægt að nota þá til staðfestingar sem hluta af frágangsferlinu sem fylgir í kjölfarið og framtíðartínsluaðgerðum.</span><span class="sxs-lookup"><span data-stu-id="9600c-108">They can then be used for validation as part of the put-away process that follows and future outbound picking operations.</span></span>

<span data-ttu-id="9600c-109">Þú getur prentað mjög flókna merkimiða, að því tilskildu að prentunarbúnaðurinn geti túlkað textann sem er sendur til hans.</span><span class="sxs-lookup"><span data-stu-id="9600c-109">You can print highly complex labels, provided that the printing device can interpret the text that is sent to it.</span></span> <span data-ttu-id="9600c-110">Til dæmis gæti skipulag forritunarmálsins Zebra (ZPL) sem inniheldur strikamerki líkst eftirfarandi dæmi.</span><span class="sxs-lookup"><span data-stu-id="9600c-110">For example, a Zebra Programming Language (ZPL) layout that includes a bar code might resemble the following example.</span></span>

```dos
^XA~TA000~JSN^LT0^MNW^MTD^PON^PMN^LH0,0^JMA^PR2,2~SD15^JUS^LRN^CI0^XZ
^XA
^MMT
^PW320
^LL0160
^LS0
^FT20,58^A0N,28,28^FH\^FDLabel:^FS
^FT20,81^AAN,18,10^FH\^FD$LicensePlateId$^FS
^BY1,3,17^FT20,106^BCN,,Y,N,N,A
^FD$LicensePlateId$^FS
^PQ1,,,Y^XZ
```

<span data-ttu-id="9600c-111">Sem hluti af prentunarferlinu verður textanum `$LicensePlateId$` í þessu dæmi skipt út fyrir gagnagildi.</span><span class="sxs-lookup"><span data-stu-id="9600c-111">As part of the label printing process, the text `$LicensePlateId$` in this example will be replaced with a data value.</span></span>

<span data-ttu-id="9600c-112">Til að sjá gildin sem verða prentuð ferðu á **Vöruhúsastjórnun \> Fyrirspurnir og skýrslur \> Merkimiðar á númeraplötum**.</span><span class="sxs-lookup"><span data-stu-id="9600c-112">To see the values that will be printed, go to **Warehouse management \> Inquiries and reports \> License plate labels**.</span></span>

<span data-ttu-id="9600c-113">Nokkur víðtækt fáanleg verkfæri til merkjamyndunar geta hjálpað þér að forsníða textann fyrir útlit merkisins.</span><span class="sxs-lookup"><span data-stu-id="9600c-113">Several widely available label generation tools can help you format the text for the label layout.</span></span> <span data-ttu-id="9600c-114">Mörg þessara verkfæra styðja sniðið `$FieldName$`.</span><span class="sxs-lookup"><span data-stu-id="9600c-114">Many of these tools support the `$FieldName$` format.</span></span> <span data-ttu-id="9600c-115">Að auki notar Microsoft Dynamics 365 Supply Chain Management sérstaka sniðrökfræði sem hluta af reitavörpun fyrir uppsetningu skjalaleiðar.</span><span class="sxs-lookup"><span data-stu-id="9600c-115">In addition, Microsoft Dynamics 365 Supply Chain Management uses special formatting logic as part of the field mapping for the document routing layout.</span></span>

## <a name="custom-number-formats"></a><span data-ttu-id="9600c-116">Sérsniðin tölusnið</span><span class="sxs-lookup"><span data-stu-id="9600c-116">Custom number formats</span></span>

<span data-ttu-id="9600c-117">Þú getur sérsniðið snið á tölulegum reitagildum sem eru prentuð með kóða með eftirfarandi sniði.</span><span class="sxs-lookup"><span data-stu-id="9600c-117">You can customize the formatting of numerical field values that are printed by using codes that have the following format.</span></span>

```dos
$FieldName:FormatString$
```

<span data-ttu-id="9600c-118">Hér er útskýring á þessu sniði:</span><span class="sxs-lookup"><span data-stu-id="9600c-118">Here is an explanation of this format:</span></span>

- <span data-ttu-id="9600c-119">`FieldName` er heiti gagnareitsins (eins og **Magn**).</span><span class="sxs-lookup"><span data-stu-id="9600c-119">`FieldName` is the name of the data field (such as **Qty**).</span></span>
- <span data-ttu-id="9600c-120">`FormatString` skilgreinir hvernig prenta verður gögnin.</span><span class="sxs-lookup"><span data-stu-id="9600c-120">`FormatString` defines how the data must be printed.</span></span>

<span data-ttu-id="9600c-121">Eftirfarandi dæmi sýna hvernig þú getur sérsniðið vinnumagnsreitinn (**Magn**):</span><span class="sxs-lookup"><span data-stu-id="9600c-121">The following examples show how you can customize the work quantity (**Qty**) field:</span></span>

- <span data-ttu-id="9600c-122">Til að sýna alltaf fjóra tölustafi (með því að nota núll sem frátökutákn) notarðu `$Qty:0000$`.</span><span class="sxs-lookup"><span data-stu-id="9600c-122">To always show four digits (by using zeros as placeholders), use `$Qty:0000$`.</span></span> <span data-ttu-id="9600c-123">Til dæmis, ef magnið er 10 mun merkimiðinn sýna „0010”.</span><span class="sxs-lookup"><span data-stu-id="9600c-123">For example, if the quantity is 10, the label will show "0010."</span></span>
- <span data-ttu-id="9600c-124">Til að sýna alltaf tvo aukastafi notarðu `$Qty:0.00$`.</span><span class="sxs-lookup"><span data-stu-id="9600c-124">To always show two decimal places, use `$Qty:0.00$`.</span></span> <span data-ttu-id="9600c-125">Til dæmis, ef magnið er 10 mun merkimiðinn sýna „10,00”.</span><span class="sxs-lookup"><span data-stu-id="9600c-125">For example, if the quantity is 10, the label will show "10.00."</span></span>

<span data-ttu-id="9600c-126">Fyrir fullan lista yfir tiltæka strengi tölusniðmáts, sjá [Sérsniðnir strengir tölusniðmáta](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).</span><span class="sxs-lookup"><span data-stu-id="9600c-126">For a complete list of the available number format strings, see [Custom numeric format strings](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).</span></span>

## <a name="custom-string-formats"></a><span data-ttu-id="9600c-127">Sérsniðin strengjasnið</span><span class="sxs-lookup"><span data-stu-id="9600c-127">Custom string formats</span></span>

<span data-ttu-id="9600c-128">Þú getur fjarlægt fyrstu stafina í strengnum með því að nota eftirfarandi reit og sniðkóða.</span><span class="sxs-lookup"><span data-stu-id="9600c-128">You can remove the first characters of a string by using the following field and format code.</span></span>

```dos
$FieldName:#..$
```

<span data-ttu-id="9600c-129">Hér tilgreinir `#` fjölda stafa sem á að sleppa.</span><span class="sxs-lookup"><span data-stu-id="9600c-129">Here, `#` specifies the number of characters to skip.</span></span> <span data-ttu-id="9600c-130">Til dæmis, til að prenta númeraplötunúmer raðnúmers vörusendinga (SSCC) sem ekki eru fyrstu tveir stafirnir, notarðu `$LicensePlateId:2..$`.</span><span class="sxs-lookup"><span data-stu-id="9600c-130">For example, to print a Serial Shipping Container Code (SSCC) license plate number that doesn't include the first two characters, use `$LicensePlateId:2..$`.</span></span> <span data-ttu-id="9600c-131">Í þessu tilfelli verður númeraplötunúmerið 0011111111111222221 prentað sem „11111111111222221”.</span><span class="sxs-lookup"><span data-stu-id="9600c-131">In this case, the license plate number 0011111111111222221 will be printed as "11111111111222221."</span></span>

## <a name="custom-datetime-formats"></a><span data-ttu-id="9600c-132">Sérsniðin dagsetningar-/tímasnið</span><span class="sxs-lookup"><span data-stu-id="9600c-132">Custom date/time formats</span></span>

<span data-ttu-id="9600c-133">Eftirfarandi dæmi sýnir hvernig þú getur stjórnað sniðinu sem er notað til að prenta dagsetningar.</span><span class="sxs-lookup"><span data-stu-id="9600c-133">The following example shows how you can control the format that is used to print dates.</span></span>

```dos
$PrintedDate:dd-MM-yyyy$
```

<span data-ttu-id="9600c-134">Í þessu dæmi verður dagsetningin 30. apríl 2020 prentuð sem „30-04-2020”.</span><span class="sxs-lookup"><span data-stu-id="9600c-134">In this example, the date April 30, 2020, will be printed as "30-04-2020."</span></span>

<span data-ttu-id="9600c-135">Fyrir fullan lista yfir tiltæka strengi dagsetningar-/tímasniðmáta, sjá [Sérsniðnir strengir dagsetningar- og tímasniðmáta](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).</span><span class="sxs-lookup"><span data-stu-id="9600c-135">For a complete list of the available date/time formats, see [Custom date and time format strings](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).</span></span>

## <a name="print-individual-lines-from-multiline-data"></a><span data-ttu-id="9600c-136">Prentaðu einstakar línur úr samvalsgögnum</span><span class="sxs-lookup"><span data-stu-id="9600c-136">Print individual lines from multiline data</span></span>

<span data-ttu-id="9600c-137">Ef gagnareitur inniheldur margar línur (það er að segja línur sem eru aðskildar með línuskilum) geturðu prentað einstaka línu með eftirfarandi sniði.</span><span class="sxs-lookup"><span data-stu-id="9600c-137">If a data field contains multiple lines (that is, lines that are separated by line breaks), you can print an individual line by using the following format.</span></span>

```dos
$FieldName[#]$
```

<span data-ttu-id="9600c-138">Hér er `#` línunúmerið sem þú vilt prenta.</span><span class="sxs-lookup"><span data-stu-id="9600c-138">Here, `#` is the line number that you want to print.</span></span> <span data-ttu-id="9600c-139">(Notaðu 1 fyrir fyrstu línuna.)</span><span class="sxs-lookup"><span data-stu-id="9600c-139">(Use 1 for the first line.)</span></span>

<span data-ttu-id="9600c-140">Til dæmis, kerfið þitt er með reitinn `AdditionalAddress` sem geymir eftirfarandi samvalsheimilisfang:</span><span class="sxs-lookup"><span data-stu-id="9600c-140">For example, your system has an `AdditionalAddress` field that stores the following multiline address:</span></span>

<span data-ttu-id="9600c-141">Contoso Inc.</span><span class="sxs-lookup"><span data-stu-id="9600c-141">Contoso Inc.</span></span>  
<span data-ttu-id="9600c-142">123 Götuheiti</span><span class="sxs-lookup"><span data-stu-id="9600c-142">123 Street Name</span></span>  
<span data-ttu-id="9600c-143">Einhver borg, eitthvað ríki</span><span class="sxs-lookup"><span data-stu-id="9600c-143">Some City, Some State</span></span>

<span data-ttu-id="9600c-144">Þú getur prentað þetta heimilisfang, eina línu í einu, með því að nota eftirfarandi kóða.</span><span class="sxs-lookup"><span data-stu-id="9600c-144">You can print this address, one line at a time, by using the following codes.</span></span>

| <span data-ttu-id="9600c-145">Kóði</span><span class="sxs-lookup"><span data-stu-id="9600c-145">Code</span></span> | <span data-ttu-id="9600c-146">Texti sem er prentaður</span><span class="sxs-lookup"><span data-stu-id="9600c-146">Text that is printed</span></span> |
|---|---|
| `$AdditionalAddress[1]$` | <span data-ttu-id="9600c-147">Contoso Inc.</span><span class="sxs-lookup"><span data-stu-id="9600c-147">Contoso Inc.</span></span> |
| `$AdditionalAddress[2]$` | <span data-ttu-id="9600c-148">123 Götuheiti</span><span class="sxs-lookup"><span data-stu-id="9600c-148">123 Street Name</span></span> |
| `$AdditionalAddress[3]$` | <span data-ttu-id="9600c-149">Einhver borg, eitthvað ríki</span><span class="sxs-lookup"><span data-stu-id="9600c-149">Some City, Some State</span></span> |

## <a name="print-and-format-from-a-display-method"></a><span data-ttu-id="9600c-150">Prenta og sníða úr birtingaraðferð</span><span class="sxs-lookup"><span data-stu-id="9600c-150">Print and format from a display method</span></span>

<span data-ttu-id="9600c-151">Þú getur prentað úr birtingaraðferð með því að nota eftirfarandi snið.</span><span class="sxs-lookup"><span data-stu-id="9600c-151">You can print from a display method by using the following format.</span></span>

```dos
$DisplayMethod()$
```

<span data-ttu-id="9600c-152">Þú getur sameinað þetta snið við aðrar gerðir sem lýst var fyrr í þessu efni.</span><span class="sxs-lookup"><span data-stu-id="9600c-152">You can combine this format with other types that were described earlier in this topic.</span></span> <span data-ttu-id="9600c-153">Til dæmis ertu með skjáaðferð sem heitir `DisplayListOfItemsNumbers()` og þú vilt prenta fyrsta vörunúmer þessarar aðferðar.</span><span class="sxs-lookup"><span data-stu-id="9600c-153">For example, you have a display method that is named `DisplayListOfItemsNumbers()`, and you want to print the first item number of this method.</span></span> <span data-ttu-id="9600c-154">Í þessu tilviki er hægt að nota eftirfarandi kóða.</span><span class="sxs-lookup"><span data-stu-id="9600c-154">In this case, you can use the following code.</span></span>

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a><span data-ttu-id="9600c-155">Nánari upplýsingar um hvernig á að prenta merkingar</span><span class="sxs-lookup"><span data-stu-id="9600c-155">More information about how to print labels</span></span>

<span data-ttu-id="9600c-156">Nánari upplýsingar um hvernig á að setja upp og prenta merkimiða, sjá [Virkja prentun merkis á númeraplötu](tasks/license-plate-label-printing.md).</span><span class="sxs-lookup"><span data-stu-id="9600c-156">For more information about how to set up and print labels, see [Enable license plate label printing](tasks/license-plate-label-printing.md).</span></span>
