---
title: Úrræðaleita Dynamics 365-greiðslutengil fyrir vandamál varðandi Adyen
description: Þetta efnisatriði veitir leiðsögn um úrræðaleit sem getur hjálpað til þegar vandamál koma upp varðandi Microsoft Dynamics 365-greiðslutengil fyrir Adyen.
author: Reza-Assadi
manager: AnnBe
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f01db3fa670355696c094be544775a3abc557a70
ms.sourcegitcommit: 6c108be3378b365e6ec596a1a8666d59b758db25
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 03/12/2021
ms.locfileid: "5585368"
---
# <a name="troubleshoot-dynamics-365-payment-connector-for-adyen-issues"></a><span data-ttu-id="a0d27-103">Úrræðaleita Dynamics 365-greiðslutengil fyrir vandamál varðandi Adyen</span><span class="sxs-lookup"><span data-stu-id="a0d27-103">Troubleshoot Dynamics 365 Payment Connector for Adyen issues</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a0d27-104">Þetta efnisatriði veitir leiðsögn um úrræðaleit sem getur hjálpað til þegar vandamál koma upp varðandi Microsoft Dynamics 365-greiðslutengil fyrir Adyen.</span><span class="sxs-lookup"><span data-stu-id="a0d27-104">This topic provides troubleshooting guidance that can help you get support when you have issues with the Microsoft Dynamics 365 Payment Connector for Adyen.</span></span>

## <a name="description"></a><span data-ttu-id="a0d27-105">lýsing</span><span class="sxs-lookup"><span data-stu-id="a0d27-105">Description</span></span>

<span data-ttu-id="a0d27-106">Vandamál kom upp farðandi greiðslutengil Dynamics 365 fyrir Adyen á eftirfarandi svæðum og þörf er á aðstoð frá Adyen-teyminu:</span><span class="sxs-lookup"><span data-stu-id="a0d27-106">You have issues with the Dynamics 365 Payment Connector for Adyen in the following areas, and you require support from the Adyen team:</span></span>

- <span data-ttu-id="a0d27-107">Grunnstilling sölustaðar (POS), nútímasölustaðar (MPOS) símavers eða Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="a0d27-107">Configuration of Point of sale (POS), Modern point of sale (MPOS), call center, or Dynamics 365 Commerce</span></span>
- <span data-ttu-id="a0d27-108">Tilvísunarnúmer Adyen-greiðsluþjónustuveitu (PSP) (til dæmis ef vakna spurningar um hafnanir, þ.m.t. hafnanir á handvirkum lyklainnslætti \[MKE\])</span><span class="sxs-lookup"><span data-stu-id="a0d27-108">The Adyen payment service provider (PSP) reference number (for example, if you have questions about refusals, including manual key entry \[MKE\] refusals)</span></span>
- <span data-ttu-id="a0d27-109">Allt það sem virkar ekki í prófunarumhverfi eða virku umhverfi söluaðila</span><span class="sxs-lookup"><span data-stu-id="a0d27-109">Anything that isn't working in test or live merchant environments</span></span>

## <a name="resolution"></a><span data-ttu-id="a0d27-110">Upplausn</span><span class="sxs-lookup"><span data-stu-id="a0d27-110">Resolution</span></span>

<span data-ttu-id="a0d27-111">Notið eftirfarandi tölvupóstssniðmát til að hefja ferli notendaþjónustu hjá Adyen-teyminu.</span><span class="sxs-lookup"><span data-stu-id="a0d27-111">Use the following email template to start the support process with the Adyen team.</span></span> <span data-ttu-id="a0d27-112">Til að flýta fyrir úrræðaleit skal ganga úr skugga um tölvupósturinn innihaldi allar nauðsynlegar upplýsingar.</span><span class="sxs-lookup"><span data-stu-id="a0d27-112">To expedite troubleshooting, make sure that the email contains all the required details.</span></span>

| <span data-ttu-id="a0d27-113">Svæði</span><span class="sxs-lookup"><span data-stu-id="a0d27-113">Field</span></span>        | <span data-ttu-id="a0d27-114">Virði</span><span class="sxs-lookup"><span data-stu-id="a0d27-114">Value</span></span> |
|--------------|-------|
| <span data-ttu-id="a0d27-115">Að</span><span class="sxs-lookup"><span data-stu-id="a0d27-115">To</span></span>           | `support@adyen.com` |
| <span data-ttu-id="a0d27-116">Cc</span><span class="sxs-lookup"><span data-stu-id="a0d27-116">Cc</span></span>           | |
| <span data-ttu-id="a0d27-117">Efnislína</span><span class="sxs-lookup"><span data-stu-id="a0d27-117">Subject line</span></span> | <span data-ttu-id="a0d27-118">Microsoft Dynamics Þjónustubeiðni </span><span class="sxs-lookup"><span data-stu-id="a0d27-118">Microsoft Dynamics Support Request</span></span> |
| <span data-ttu-id="a0d27-119">Meginmál</span><span class="sxs-lookup"><span data-stu-id="a0d27-119">Body</span></span>         | <p><span data-ttu-id="a0d27-120">Halló notendaþjónusta,</span><span class="sxs-lookup"><span data-stu-id="a0d27-120">Hi Support,</span></span></p><p><span data-ttu-id="a0d27-121">Vinsamlegast veitið aðstoð vegna eftirfarandi vandamáls:</span><span class="sxs-lookup"><span data-stu-id="a0d27-121">Please provide support for the following issue:</span></span></p><ul><li><span data-ttu-id="a0d27-122">Lykill söluaðila</span><span class="sxs-lookup"><span data-stu-id="a0d27-122">Merchant account</span></span></li><li><span data-ttu-id="a0d27-123">Umhverfi (prófun/framleiðsla)</span><span class="sxs-lookup"><span data-stu-id="a0d27-123">Environment (Test/Prod)</span></span></li><li><span data-ttu-id="a0d27-124">Rás (sölustaður/símaver/rafræn viðskipti)</span><span class="sxs-lookup"><span data-stu-id="a0d27-124">Channel (POS/call center/Commerce e-commerce)</span></span></li><li><span data-ttu-id="a0d27-125">PSP-tilvísunarnúmer ef vandamálið tengdist ákveðinni færslu (hægt er að finna PSP-tilvísunarnúmerið á kvittuninni, á viðskiptavinasvæði Adyen, eða færsluvalmyndinni í afgreiðslukassanum.)</span><span class="sxs-lookup"><span data-stu-id="a0d27-125">PSP reference number, if the issue involved a specific transaction (You can find the PSP reference number on the receipt, in the Adyen Customer Area, or on the transactions menu on the POS terminal.)</span></span></li><li><span data-ttu-id="a0d27-126">Skjámynd eða ljósmynd af villuboðinu ef það á við</span><span class="sxs-lookup"><span data-stu-id="a0d27-126">Screenshot or photo of the error message, if applicable</span></span></li><li><span data-ttu-id="a0d27-127">Kladdar atvikaskoðunar (á .txt-sniði)</span><span class="sxs-lookup"><span data-stu-id="a0d27-127">Event Viewer logs (in .txt format)</span></span></li><li><span data-ttu-id="a0d27-128">Lýsing á vandamálinu og skref úrræðaleitar sem búið er að reyna</span><span class="sxs-lookup"><span data-stu-id="a0d27-128">Description of the issue and troubleshooting steps that you've tried</span></span></li></ul> |

## <a name="additional-resources"></a><span data-ttu-id="a0d27-129">Frekari upplýsingar</span><span class="sxs-lookup"><span data-stu-id="a0d27-129">Additional resources</span></span>

[<span data-ttu-id="a0d27-130">Samþykkja greiðslur með Adyen-tengli fyrir Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="a0d27-130">Accept payments with the Adyen connector for Dynamics 365 Commerce</span></span>](https://www.adyen.com/partners/dynamics-365-commerce)

[<span data-ttu-id="a0d27-131">Dynamics 365-greiðslutengill fyrir Adyen</span><span class="sxs-lookup"><span data-stu-id="a0d27-131">Dynamics 365 Payment Connector for Adyen</span></span>](../dev-itpro/adyen-connector.md)

[<span data-ttu-id="a0d27-132">Setja upp Adyen-greiðslutengil fyrir Dynamics 365</span><span class="sxs-lookup"><span data-stu-id="a0d27-132">Set up the Adyen payment connector for Dynamics 365</span></span>](https://docs.adyen.com/plugins/microsoft-dynamics)
