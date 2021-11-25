---
title: Sérsníða viðmót fyrir framkvæmd á framleiðslugólfi
description: Þetta efnisatriði útskýrir hvernig á að framlengja núverandi eyðublöð eða búa til ný eyðublöð og hnappa fyrir framkvæmdarviðmót framleiðslugólfs.
author: johanhoffmann
ms.date: 11/08/2021
ms.topic: article
ms.search.form: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-11-08
ms.dyn365.ops.version: 10.0.24
ms.openlocfilehash: 414fe5d6e16ad125bc2b9bb7ed427e5db5180ec9
ms.sourcegitcommit: bc9e75c38e192664cde226ed3a94df5a0b304369
ms.translationtype: MT
ms.contentlocale: is-IS
ms.lasthandoff: 11/10/2021
ms.locfileid: "7790976"
---
# <a name="customize-the-production-floor-execution-interface"></a>Sérsníða viðmót fyrir framkvæmd á framleiðslugólfi

[!include [banner](../includes/banner.md)]

Hönnuðir geta framlengt núverandi eyðublöð eða búið til sín eigin eyðublöð og hnappa fyrir framkvæmdarviðmót framleiðslugólfsins. Eftir að þú hefur bætt kóðanum fyrir þessa nýju þætti geta stjórnendur eða verslunarstjórar auðveldlega bætt þeim við viðmótið með því að nota staðlaðar stillingarstýringar.

Hér eru til dæmis nokkrar mögulegar lausnir ef þörf er á nýjum dálkum í aðalformi:

- Framlengdu`JmgProductionFloorExecutionMainGrid` eyðublað og bættu við reitunum sem þú vilt.
- Búðu til nýtt eyðublað og bættu því við sem nýjum aðalskjá (flipi).

## <a name="add-a-new-button-action"></a>Bæta við nýjum hnappi (aðgerð)

Til að bæta við nýjum hnappi (aðgerð) skaltu fylgja þessum skrefum til að búa til flokk sem útfærir sérsniðna aðgerðina þína.

1. Búðu til nýjan flokk sem heitir`<ExtensionPrefix>_JmgProductionFloorExecution<ActionName>Action`, hvar:

    - `<ExtensionPrefix>` auðkennir lausnina þína einstaklega, venjulega með því að nota nafn fyrirtækis þíns.
    - `<ActionName>` er einstakt nafn fyrir bekkinn. Það auðkennir venjulega tegund aðgerða.

1. Nýi flokkurinn verður að lengja`JmgProductionFloorExecutionAction` bekk.
1. Hneka allar nauðsynlegar aðferðir.

Fyrir dæmi, skoðaðu kóðann fyrir eftirfarandi flokka:

- `JmgProductionFloorExecutionBreakAction`– Flokkur fyrir einfalda aðgerð sem þarfnast engar skrár.
- `JmgProductionFloorExecutionReportFeedbackAction`– Klassi sem veitir flóknari virkni.

Þegar þú ert búinn verður nýi hnappurinn (aðgerðin) sjálfkrafa skráður á **Hönnunarflipar** síðu í Microsoft Dynamics 365 Supply Chain Management. Þar getur þú (eða stjórnandi eða gólfstjóri) auðveldlega bætt því við aðal- eða aukatækjastikuna, rétt eins og þú getur bætt við stöðluðum hnöppum. Fyrir leiðbeiningar, sjá [Hannaðu framkvæmdarviðmót framleiðslugólfsins](production-floor-execution-tabs.md).

## <a name="add-a-new-main-view"></a>Bættu við nýjum aðalskjá

1. Búðu til nýtt eyðublað sem hefur viðeigandi þætti og virkni. Athugaðu að þetta eyðublað er nýtt eyðublað, ekki viðbót. Nefndu formið`<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`, hvar:

    - `<ExtensionPrefix>` auðkennir lausnina þína einstaklega, venjulega með því að nota nafn fyrirtækis þíns.
    - `<FormName>` er einstakt heiti á forminu.

1. Búðu til valmyndaratriði sem er nefnt `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`.
1. Búðu til viðbót sem er nefnd`<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension`, þar sem`getMainMenuItemsList` aðferð er framlengd með því að bæta nýja valmyndaratriðinu við listann. Eftirfarandi kóði sýnir dæmi.

    ```xpp
    [ExtensionOf(classStr(JmgProductionFloorExecutionForm))]
    public final class <ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>_Extension{
        static public List getMainMenuItemsList()
        {
            List menuItemList = next getMainMenuItemsList();
            menuItemList.addEnd(menuItemDisplayStr(<ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>));
            return menuItemList;
        }
    ```

Þegar þú ert búinn verður nýja aðalskjárinn sjálfkrafa skráður í **Aðalsýn** combo kassi á **Hönnunarflipar** síðu í Supply Chain Management. Þar getur þú (eða stjórnandi eða gólfstjóri) auðveldlega bætt því við nýja eða núverandi flipa, rétt eins og þú getur bætt við venjulegum aðalsýnum. Fyrir leiðbeiningar, sjá [Hannaðu framkvæmdarviðmót framleiðslugólfsins](production-floor-execution-tabs.md).

## <a name="add-a-details-view"></a>Bættu við upplýsingaskjá

1. Búðu til nýtt eyðublað sem hefur viðeigandi þætti og virkni. Athugaðu að þetta eyðublað er nýtt, ekki viðbót. Nefndu formið`<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`, hvar: 

    - `<ExtensionPrefix>` auðkennir lausnina þína einstaklega, venjulega með því að nota nafn fyrirtækis þíns.
    - `<FormName>` er einstakt heiti á forminu.

1. Búðu til valmyndaratriði sem er nefnt `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`.
1. Búðu til viðbót sem er nefnd`<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension`, þar sem`getDetailsMenuItemList` aðferð er framlengd með því að bæta nýja valmyndaratriðinu við listann.

Þegar þú ert búinn verður nýja upplýsingaskjárinn sjálfkrafa skráður í **Upplýsingar skoða** combo kassi á **Hönnunarflipar** síðu í Supply Chain Management. Þar getur þú (eða stjórnandi eða gólfstjóri) auðveldlega bætt því við nýja eða núverandi flipa, rétt eins og þú getur bætt við stöðluðum upplýsingasýnum. Fyrir leiðbeiningar, sjá [Hannaðu framkvæmdarviðmót framleiðslugólfsins](production-floor-execution-tabs.md).

## <a name="add-a-numeric-keypad-to-a-form-or-dialog"></a>Bættu talnatakkaborði við eyðublað eða glugga

Eftirfarandi dæmi sýnir hvernig á að bæta tölutakkaborðum við eyðublað.

1. Fjöldi talnatakkaborðsstýringa sem hvert eyðublað inniheldur verður að jafna fjölda talnatakkaborða á því formi.

    ```xpp
    private JmgProductionFloorExecutionNumpadController   numpadController1;
    private JmgProductionFloorExecutionNumpadController   numpadController2;
    private JmgProductionFloorExecutionNumpadController   numpadController3;
    ```

1. Settu upp hegðun hvers talnatakkaborðsstýringar og tengdu hvern talnatakkaborðsstýringu við talnatakkaborðshluta.

    ```xpp
    /// <summary>
    /// Initializes all numpad controllers, defines their behavior and connects them with numpad form parts.
    /// </summary>
    public void initializeNumpadController()
    {
        numpadController1 = new JmgProductionFloorExecutionNumpadController();
        numpadController1.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_1);
        QuantityNumpad1.getPartFormRun().setNumpadController(numpadController1);
    
        numpadController2 = new JmgProductionFloorExecutionNumpadController();
        numpadController2.parmNumpadEnabled(false);
        numpadController2.parmNumpadValue(333.56);
        numpadController2.getValueFromNumpadDelegate += eventhandler(this.setQuanityValueFromNumpad_2);
        QuantityNumpad2.getPartFormRun().setNumpadController(numpadController2);
    }
    ```

## <a name="use-a-numeric-keypad-as-a-pop-up-dialog"></a>Notaðu talnatakkaborð sem sprettiglugga

Eftirfarandi dæmi sýnir eina leið til að setja upp talnatakkaborðsstýringu fyrir sprettiglugga.

```xpp
private void setupNumpadController()
{
    numpadController = new JmgProductionFloorExecutionNumpadController();
    numpadController.parmShouldNumpadShowOkCancelButtons(true);
    numpadController.setNumpadValueToParentFormDelegate += eventhandler(this.setQtyValueFromNumpad);
}
```

Eftirfarandi dæmi sýnir eina leið til að hringja í sprettigluggan talnaborðsins.

```xpp
Args args = new Args();
args.name(formstr(JmgProductionFloorExecutionNumpad));
args.menuItemName(menuItemDisplayStr(JmgProductionFloorExecutionNumpad));
args.caller(element);
Object formRun = classfactory.formRunClass(args);
formRun.init();
formRun.setNumpadController(numpadController);
numpadController.setValueToNumpad(333.56);
formRun.run();
```

## <a name="additional-resources"></a>Frekari upplýsingar

- [Hanna keyrsluviðmót framleiðslugólfsins](production-floor-execution-styles.md)
- [Hanna viðmótið fyrir framkvæmd á framleiðslugólfi](production-floor-execution-tabs.md)
