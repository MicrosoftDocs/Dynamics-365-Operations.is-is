---
title: Aðgerð skiptingar á reikningi
description: Í þessu efnisatriði er útskýrð uppsetning og virkni fyrir skiptingu reikninga eftir afhendingaraðsetri og skattlykilnúmeri (TAN).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 7dddbb9f69a9735c2a03d2b23928f5cb92d4e0fd
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023333"
---
# <a name="split-invoice-functionality"></a><span data-ttu-id="9c213-103">Aðgerð skiptingar á reikningi</span><span class="sxs-lookup"><span data-stu-id="9c213-103">Split invoice functionality</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c213-104">Í þessu efnisatriði er útskýrð uppsetning og virkni fyrir skiptingu reikninga eftir afhendingaraðsetri og skattlykilnúmeri (TAN).</span><span class="sxs-lookup"><span data-stu-id="9c213-104">This topic describes the setup and functionality for splitting invoices by delivery address and tax account number (TAN).</span></span>

<span data-ttu-id="9c213-105">Á síðunni **Færibreytur viðskiptaskulda**, í flipanum **Almennt**, skal velja gátreitinn **Innhreyfingarskjal afurðar** eða **Reikningur** til að bóka og skipta innhreyfingarskjali afurðar eða reikningi sem er með annað afhendingaraðsetur og TAN á síðunni **Innkaupapöntun**.</span><span class="sxs-lookup"><span data-stu-id="9c213-105">On the **Accounts payable parameters** page, on the **General** tab, select the **Product receipt** or **Invoice** checkbox to post and split a product receipt or invoice that has different delivery addresses and TANs on the **Purchase order** page.</span></span> <span data-ttu-id="9c213-106">Bókuðum reikningi verður þá skipt eftir afhendingaraðsetri og TAN.</span><span class="sxs-lookup"><span data-stu-id="9c213-106">The posted invoice will then be split by delivery address and TAN.</span></span>

<span data-ttu-id="9c213-107">Í flipanum **Samantektaruppfærsla**, í flýtiflipanum **Skipting byggð á**, í línunni **Afhendingarupplýsingar**, skal stilla valkostinn **Staðfesting**, **Tiltektarlisti**, **Fylgiseðill** eða **Reikningur** á **Já** til að bóka og skipta staðfestingu, tiltektarlista, fylgiseðli eða reikningi þar sem önnur afhendingaraðsetur og TAN eru skilgreind fyrir mismunandi reikningslínur á síðunni **Sölupöntun**.</span><span class="sxs-lookup"><span data-stu-id="9c213-107">On the **Summary update** tab, on the **Split based on** FastTab, in the **Delivery information** row, set the **Confirmation**, **Picking list**, **Packing slip**, or **Invoice** option to **Yes** to post and split a confirmation, picking list, packing slip, or invoice where different delivery addresses and TANs are defined for different invoice lines on the **Sales order** page.</span></span> <span data-ttu-id="9c213-108">Reikningnum verður fyrst skipt eftir afhendingaraðsetri og síðan eftir TAN.</span><span class="sxs-lookup"><span data-stu-id="9c213-108">The invoice will be split first by delivery address and then by TAN.</span></span>

> [!IMPORTANT]
> - <span data-ttu-id="9c213-109">Ef engir valkostir fyrir **Afhendingarupplýsingar** eru stilltir á **Já** verður reikningurinn bókaður sem einn reikningur.</span><span class="sxs-lookup"><span data-stu-id="9c213-109">If no options for **Delivery information** are set to **Yes**, the invoice will be posted as a single invoice.</span></span> <span data-ttu-id="9c213-110">Engin skipting á reikningi mun eiga sér stað.</span><span class="sxs-lookup"><span data-stu-id="9c213-110">No invoice splitting will occur.</span></span>
> - <span data-ttu-id="9c213-111">Til að skipta og bóka fylgiseðil þar sem reikningslínurnar eru með mismunandi afhendingaraðsetur og TAN þarf að stilla valkostinn **Fylgiseðill** fyrir **Afhendingarupplýsingar** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="9c213-111">To split and post a packing slip where the invoice lines have different delivery addresses and TANs, you must set the **Packing slip** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="9c213-112">Til að skipta og bóka reikning þar sem reikningslínurnar eru með mismunandi afhendingaraðsetur og TAN þarf að stilla valkostinn **Reikningur** fyrir **Afhendingarupplýsingar** á **Já**.</span><span class="sxs-lookup"><span data-stu-id="9c213-112">To split and post an invoice where the invoice lines have different delivery addresses and TANs, you must set the **Invoice** option for **Delivery information** to **Yes**.</span></span>
> - <span data-ttu-id="9c213-113">Til að bóka reikning þar sem reikningslínurnar eru með mismunandi afhendingaraðsetur en sama TAN skal stilla valkostinn **Reikningur** fyrir **Afhendingarupplýsingar** á **Nei**.</span><span class="sxs-lookup"><span data-stu-id="9c213-113">To post an invoice where the invoice lines have different delivery addresses but the same TAN, set the **Invoice** option for **Delivery information** to **No**.</span></span> <span data-ttu-id="9c213-114">Reikningnum verður skipt eftir afhendingaraðsetri.</span><span class="sxs-lookup"><span data-stu-id="9c213-114">The invoice will be split by delivery address.</span></span>

## <a name="example"></a><span data-ttu-id="9c213-115">Dæmi</span><span class="sxs-lookup"><span data-stu-id="9c213-115">Example</span></span>

<span data-ttu-id="9c213-116">Í þessu dæmi er valkosturinn **Reikningur** fyrir **Afhendingarupplýsingar** stilltur á **Já** í flipanum **Samantektaruppfærsla** á síðunni **Færibreytur viðskiptaskulda**.</span><span class="sxs-lookup"><span data-stu-id="9c213-116">In this example, the **Invoice** option for **Delivery information** is set to **Yes** on the **Summary update** tab of the **Accounts payable parameters** page.</span></span> <span data-ttu-id="9c213-117">Innkaupareikningur er bókaður sem er með eftirfarandi uppsetningu fyrir afhendingaraðsetur og TAN í línunum:</span><span class="sxs-lookup"><span data-stu-id="9c213-117">A purchase invoice is posted that has the following setup for delivery addresses and TANs on the lines:</span></span>

- <span data-ttu-id="9c213-118">**Vörulína 1:** Afhendingaraðsetur 1, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="9c213-118">**Item line 1:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="9c213-119">**Vörulína 2:** Afhendingaraðsetur 1, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="9c213-119">**Item line 2:** Delivery address 1, TAN-ABCD12345A</span></span>
- <span data-ttu-id="9c213-120">**Vörulína 3:** Afhendingaraðsetur 2, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="9c213-120">**Item line 3:** Delivery address 2, TAN-ABCE12345B</span></span>
- <span data-ttu-id="9c213-121">**Vörulína 4:** Afhendingaraðsetur 3, TAN-ABCD12345A</span><span class="sxs-lookup"><span data-stu-id="9c213-121">**Item line 4:** Delivery address 3, TAN-ABCD12345A</span></span>

<span data-ttu-id="9c213-122">Í þessu tilfelli er upphaflegum reikningi skipt í tvo reikninga og hann bókaður á eftirfarandi hátt:</span><span class="sxs-lookup"><span data-stu-id="9c213-122">In this case, the original invoice is split into two invoices and posted in the following way:</span></span>

- <span data-ttu-id="9c213-123">Reikningur 1 er bókaður fyrir vörulínu 1 og vörulínu 2 vegna þess að báðar línurnar eru með sama afhendingaraðsetur og TAN.</span><span class="sxs-lookup"><span data-stu-id="9c213-123">Invoice 1 is posted for item line 1 and item line 2, because both lines have the same delivery address and TAN.</span></span>
- <span data-ttu-id="9c213-124">Reikningur 2 er bókaður fyrir vörulínu 3.</span><span class="sxs-lookup"><span data-stu-id="9c213-124">Invoice 2 is posted for item line 3.</span></span>
- <span data-ttu-id="9c213-125">Reikningur 3 er bókaður fyrir vörulínu 4.</span><span class="sxs-lookup"><span data-stu-id="9c213-125">Invoice 3 is posted for item line 4.</span></span>
