---
title: Opna sniðmát fyrir fjárhagsbók í Office
description: Þetta efnisatriði lýsir vandamálum sem gætu komið upp þegar þú býrð til sérsniðnar fjárhagsbækur með því að nota Microsoft Excel sniðmát.
author: kweekley
ms.date: 05/14/2021
ms.topic: index-page
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2020-05-14
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 0773f47551b2460ec310b92b67c634b433147749
ms.sourcegitcommit: 8c5b3e872825953853ad57fc67ba6e5ae92b9afe
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 05/24/2021
ms.locfileid: "6089458"
---
# <a name="open-financial-journal-templates-in-office"></a><span data-ttu-id="8f495-103">Opna sniðmát fyrir fjárhagsbók í Office</span><span class="sxs-lookup"><span data-stu-id="8f495-103">Open financial journal templates in Office</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8f495-104">Þetta efnisatriði lýsir vandamálum sem gætu komið upp þegar þú býrð til sérsniðnar fjárhagsbækur með því að nota Microsoft Excel sniðmát.</span><span class="sxs-lookup"><span data-stu-id="8f495-104">This topic describes issues that might occur when you create custom financial journals by using a Microsoft Excel template.</span></span>

## <a name="symptom"></a><span data-ttu-id="8f495-105">Einkenni</span><span class="sxs-lookup"><span data-stu-id="8f495-105">Symptom</span></span>

<span data-ttu-id="8f495-106">Þú bjóst til sérsniðið Excel-sniðmát fyrir fjárhagsbækur en það birtist ekki á valmyndinni **„Opna línur í Excel“**.</span><span class="sxs-lookup"><span data-stu-id="8f495-106">You created a custom Excel template for financial journals, but it doesn't appear on the **Open lines in Excel** menu.</span></span> <span data-ttu-id="8f495-107">Eða, ef það birtist það á valmyndinni, annað sniðmát er opnað en það sem þú valdir.</span><span class="sxs-lookup"><span data-stu-id="8f495-107">Alternatively, it does appear on the menu, a different template is opened but when you select it.</span></span>

## <a name="resolution"></a><span data-ttu-id="8f495-108">Lausn</span><span class="sxs-lookup"><span data-stu-id="8f495-108">Resolution</span></span>

<span data-ttu-id="8f495-109">Sjálfgefna virknin „Opna í Excel“ notar rótargagnagjafa (tafla) núverandi síðu til að ákvarða hvaða sniðmát eða gagnaeiningar Office birtast sem valkostir á valmyndinni **„Opna í Excel“**.</span><span class="sxs-lookup"><span data-stu-id="8f495-109">The default Open in Excel functionality uses the root data source (table) of the current page to determine which Office templates or data entities appear as options on the **Open in Excel** menu.</span></span> <span data-ttu-id="8f495-110">Þessi virkni hentar ekki fjárhagsbókum þar sem þær nota sömu töflur (LedgerJournalTable og LedgerJournalTrans) og rótargagnagjafar margra annarra gerða færslubóka.</span><span class="sxs-lookup"><span data-stu-id="8f495-110">This behavior isn't an ideal experience for financial journals, because financial journals use the same tables (LedgerJournalTable and LedgerJournalTrans) as the root data source of many other types of journals.</span></span>

<span data-ttu-id="8f495-111">Í tilfellum fjárhagsbóka er „Opna línur í Excel“ virkninni ætlað að sýna sniðmát sem eru hönnuð í samhengi við færslubókina sem þú ert að vinna í, t.d. almenna dagbók eða greiðsludagbók.</span><span class="sxs-lookup"><span data-stu-id="8f495-111">For financial journals, the Open Lines in Excel functionality is intended to show templates that are designed for the journal that you're currently working in the context of, such as the general journal or a payment journal.</span></span> <span data-ttu-id="8f495-112">Til dæmis er sniðmát sem er ætlað er til notkunar með greiðsludagbók söluaðila hannað til að framfylgja aðalreikningi þínum sem lánardrottnalykill.</span><span class="sxs-lookup"><span data-stu-id="8f495-112">For example, a template that is intended to be used with a vendor payment journal will be designed to enforce your primary account as a vendor account.</span></span>

<span data-ttu-id="8f495-113">Ef þú vilt kynna sniðmát svo það sé tiltækt á **„Opna línur í Excel“** og valmyndinni **„Opna línur í Excel“** er auðvelt þróunarumhverfi að innleiða **LedgerIJournalExcelTemplate** viðmótið og stækka **DocuTemplateRegistrationBase** klasann.</span><span class="sxs-lookup"><span data-stu-id="8f495-113">If you want to promote a template so that it's available on the **Open lines in Excel** and **Open in Excel** menus, an easy developer experience is to implement the **LedgerIJournalExcelTemplate** interface and extend the **DocuTemplateRegistrationBase** class.</span></span> <span data-ttu-id="8f495-114">Mörg dæmi um þessa nálgun eru í kerfinu.</span><span class="sxs-lookup"><span data-stu-id="8f495-114">Many examples of this approach are implemented in the system.</span></span> <span data-ttu-id="8f495-115">Dæmi sem má nota til viðmiðunar er **LedgerDailyJournalExcelTemplate** viðmótið sem búið var til fyrir almenna færslubók (eða daglega færslubók).</span><span class="sxs-lookup"><span data-stu-id="8f495-115">One example that can be used for reference is the **LedgerDailyJournalExcelTemplate** interface that was created for the general journal (or daily journal).</span></span>

<span data-ttu-id="8f495-116">Þegar **LedgerIJournalExcelTemplate** viðmótið er útfært fyrir sniðmátið þitt síar valmyndin **„Opna línur í Excel“** sniðmát eftir færslubókargerðinni sem þú notar og sýnir aðeins sniðmátin sem eru í boði fyrir þá færslubók.</span><span class="sxs-lookup"><span data-stu-id="8f495-116">When the **LedgerIJournalExcelTemplate** interface is implemented for your template, the **Open Lines in Excel** menu will filter templates by the journal type of your journal and will show only the templates that are available for that journal.</span></span> <span data-ttu-id="8f495-117">Viðmótið býður einnig upp á villuleitaraðferð sem tryggir að ekki sé hægt að opna sniðmát fyrir færslubók nema það uppfylli kröfur lyklagerðarinnar.</span><span class="sxs-lookup"><span data-stu-id="8f495-117">The interface also provides a validation method that ensures that a template can't be opened for a journal if it doesn't meet the account type requirements.</span></span> <span data-ttu-id="8f495-118">Til dæmis geturðu tilgreint að lyklagerðin verði að vera **„Lánardrottinn“** eða **„Fjárhagur“**.</span><span class="sxs-lookup"><span data-stu-id="8f495-118">For example, you can specify that the account type must be of the **Vendor** or **Ledger** type.</span></span>

<span data-ttu-id="8f495-119">Nánari upplýsingar um þessa virkni má nálgast á [Sniðmátum bætt við valmyndina „Opna línur í Excel“](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).</span><span class="sxs-lookup"><span data-stu-id="8f495-119">For more information about this functionality, see [Add templates to the Open lines in Excel menu](../../fin-ops-core/dev-itpro/user-interface/add-templates-open-lines-excel-menu.md).</span></span>
