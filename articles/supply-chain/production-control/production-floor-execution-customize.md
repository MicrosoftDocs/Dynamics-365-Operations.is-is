---
title: Sérsníða viðmót fyrir framkvæmd á framleiðslugólfi
description: Þessi grein útskýrir hvernig á að stækka núverandi skjámyndir eða búa til nýjar skjámyndir fyrir keyrsluviðmót framleiðslugólfs.
author: johanhoffmann
ms.date: 05/04/2022
ms.topic: article
ms.search.form: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-11-08
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 13fa6c2f3c30a820585d1b5a758f57ec563664d1
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: is-IS
ms.lasthandoff: 06/03/2022
ms.locfileid: "8845983"
---
# <a name="customize-the-production-floor-execution-interface"></a>Sérsníða viðmót fyrir framkvæmd á framleiðslugólfi

[!include [banner](../includes/banner.md)]

Hönnuðir geta framlengt núverandi form eða búið til eigin form og hnappa fyrir viðmót fyrir framkvæmd á framleiðslugólfi. Eftir að þú hefur bætt kóðanum fyrir þessa nýju þætti geta stjórnendur eða stjórnendur í vinnusal auðveldlega bætt þeim við viðmótið með því að nota hefðbundnar stillingarstýringar.

Hér eru t.d. nokkrar mögulegar lausnir ef þörf er á nýjum dálkum á aðalformi:

- Lengja `JmgProductionFloorExecutionMainGrid` formið og bæta við reitum sem óskað er eftir.
- Búa til nýtt form og bæta því við sem nýju yfirliti (flipa).

## <a name="add-a-new-button-action"></a>Bæta við nýjum hnappi (aðgerð)

Til að bæta við nýjum hnappi (aðgerð) skal fylgja þessum skrefum til að búa til klasa sem innleiðir sérsniðnu aðgerðina þína.

1. Búðu til nýjan flokk sem heitir `<ExtensionPrefix>_JmgProductionFloorExecution<ActionName>Action`, þar sem:

    - `<ExtensionPrefix>` auðkennir lausnina þína á einkvæman hátt, yfirleitt með því að nota heiti fyrirtækis þíns.
    - `<ActionName>` er einstakt heiti fyrir flokkinn. Það greinir yfirleitt hvers konar aðgerðir.

1. Nýi flokkurinn verður að lengja `JmgProductionFloorExecutionAction` flokkinn.
1. Hunsa allar nauðsynlegar aðferðir.

Til dæmis skaltu skoða kóðann fyrir eftirfarandi flokka:

- `JmgProductionFloorExecutionBreakAction` – Flokkur fyrir einfalda aðgerð sem þarfnast engra skráa.
- `JmgProductionFloorExecutionReportFeedbackAction` – Flokkur sem veitir flóknari virkni.

Að því loknu verður nýi hnappurinn (aðgerð) sjálfkrafa birtur á síðunni **Hönnunarflipar** í Microsoft Dynamics 365 Supply Chain Management. Þar getur þú (eða stjórnandi eða yfirmaður á gólfi) auðveldlega bætt honum við aðal- eða aukatækjastiku, rétt eins og hægt er að bæta við stöðluðum hnöppum. Frekari leiðbeiningar er að finna í [Hanna keyrsluviðmót framleiðslugólfs](production-floor-execution-tabs.md).

## <a name="add-a-new-main-view"></a>Bæta við nýrri aðalsýn

1. Búa til nýtt form sem hefur þá þætti og virkni sem óskað er eftir. Hafðu í huga að þetta eyðublað er nýtt eyðublað, ekki framlenging. Heiti forms `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`, þar sem:

    - `<ExtensionPrefix>` auðkennir lausnina þína á einkvæman hátt, yfirleitt með því að nota heiti fyrirtækis þíns.
    - `<FormName>` er einstakt heiti á forminu.

1. Stofnið valmyndaratriði með heitinu `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>`.
1. Búa til viðbót sem heitir`<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension`, þar sem `getMainMenuItemsList` aðferðin er framlengd með því að bæta nýja valmyndarhlutnum við listann. Eftirfarandi kóði sýnir dæmi.

    ```xpp
    [ExtensionOf(classStr(JmgProductionFloorExecutionMenuItemProvider))]
    public final class <ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>_Extension{
        static public List getMainMenuItemsList()
        {
            List menuItemList = next getMainMenuItemsList();
            menuItemList.addEnd(menuItemDisplayStr(<ExtensionPrefix>_JmgProductionFloorExecutionForm<FormName>));
            return menuItemList;
        }
    ```

Að því loknum verður nýja aðalyfirlitið sjálfkrafa sýnt í samsetta glugganum **Aðalyfirlit** á síðunni **Hönnunarflipar** í Supply Chain Management. Þar getur þú (eða stjórnandi eða yfirmaður á gólfi) auðveldlega bætt við nýjum eða fyrirliggjandi flipum, rétt eins og hægt er bæta við stöðluðum aðalyfirlitum. Frekari leiðbeiningar er að finna í [Hanna keyrsluviðmót framleiðslugólfs](production-floor-execution-tabs.md).

## <a name="add-a-details-view"></a>Bæta við upplýsingaglugga

1. Búa til nýtt form sem hefur þá þætti og virkni sem óskað er eftir. Hafðu í huga að þetta eyðublað er nýtt, ekki framlenging. Heiti forms `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`, þar sem: 

    - `<ExtensionPrefix>` auðkennir lausnina þína á einkvæman hátt, yfirleitt með því að nota heiti fyrirtækis þíns.
    - `<FormName>` er einstakt heiti á forminu.

1. Stofnið valmyndaratriði með heitinu `<ExtensionPrefix>_JmgProductionFloorExecution<FormName>Detail`.
1. Búa til viðbót sem heitir`<ExtensionPrefix>_JmgProductionFloorExecution<FormName>_Extension`, þar sem `getDetailsMenuItemList` aðferðin er framlengd með því að bæta nýja valmyndarhlutnum við listann.

Að því loknum verður nýja aðalyfirlitið sjálfkrafa sýnt í samsetta glugganum **Upplýsingayfirlit** á síðunni **Hönnunarflipar** í Supply Chain Management. Þar getur þú (eða stjórnandi eða yfirmaður á gólfi) auðveldlega bætt því við nýja eða fyrirliggjandi flipa, rétt eins og hægt er að bæta við stöðluðum upplýsingayfirlitum. Frekari leiðbeiningar er að finna í [Hanna keyrsluviðmót framleiðslugólfs](production-floor-execution-tabs.md).

## <a name="add-a-numeric-keypad-to-a-form-or-dialog"></a>Bæta við talnaborði í glugga eða formi

Eftirfarandi dæmi sýnir hvernig á að bæta við talnalyklaborðum á eyðublað.

1. Fjöldi talnaborðsstýringa sem hver skjámynd inniheldur verður að vera jafn fjölda talnaborða í skjámyndinni.

    ```xpp
    private JmgProductionFloorExecutionNumpadController   numpadController1;
    private JmgProductionFloorExecutionNumpadController   numpadController2;
    private JmgProductionFloorExecutionNumpadController   numpadController3;
    ```

1. Setja upp hegðun hverrar talnalyklaborðsstýringar og tengja hverja talnalyklaborðsstýringu við formhluta talnaborðs.

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

## <a name="use-a-numeric-keypad-as-a-pop-up-dialog"></a>Nota talnaborð sem sprettiglugga

Eftirfarandi dæmi sýnir eina leið til að setja upp talnahnappastýringu fyrir sprettiglugga.

```xpp
private void setupNumpadController()
{
    numpadController = new JmgProductionFloorExecutionNumpadController();
    numpadController.parmShouldNumpadShowOkCancelButtons(true);
    numpadController.setNumpadValueToParentFormDelegate += eventhandler(this.setQtyValueFromNumpad);
}
```

Eftirfarandi dæmi sýnir eina leið til að kalla á sprettiglugga talnaborðsins.

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

## <a name="add-a-date-and-time-controls-to-a-form-or-dialog"></a>Bæta við dagsetningu og for í glugga

Þessi hluti sýnir hvernig á að bæta dagsetningar- og tímastýringum við skjámynd eða svarglugga. Snertivænar stýringar fyrir dag og tíma gera starfskröftum kleift að tilgreina dagsetningar og tíma. Eftirfarandi skjámyndir sýna hvernig stjórntækin birtast yfirleitt á síðunni. Tímastýringin býður upp á bæði 12 tíma og 24 tíma útgáfur; birt útgáfa mun fylgja kjörstillingum fyrir notandareikninginn þar sem viðmótið er keyrt.

![Dæmi um dagsetningarstýringu.](media/pfe-customize-date-control.png "Dæmi um dagsetningarstýringu")

![Tímastýringardæmi með 12 tíma klukku.](media/pfe-customize-time-control-12h.png "Tímastýringardæmi með 12 tíma klukku")

![Tímastýringardæmi með 24 tíma klukku.](media/pfe-customize-time-control-24h.png "Tímastýringardæmi með 24 tíma klukku")

Aðferðin sem notuð er hér á eftir sýnir dæmi um hvernig hægt er að bæta dagsetninga- og tímastýringum við eyðublað.

1. Bætið stýringu við formið fyrir hverja stýringu dagsetningar og tíma sem formið ætti að innihalda. (Fjöldi stýringa verður að vera jafn og fjöldi dag- og tímastýringa á forminu.)

    ```xpp
    private JmgProductionFloorExecutionDateTimeController  dateFromController; 
    private JmgProductionFloorExecutionDateTimeController  dateToController; 
    private JmgProductionFloorExecutionDateTimeController  timeFromController; 
    private JmgProductionFloorExecutionDateTimeController  timeToController;
    ```

1. Lýsið nauðsynlegum breytum (af gerð `utcdatetime`).

    ```xpp
    private utcdatetime fromDateTime;
    private utcdatetime toDateTime;
    ```

1. Búa til aðferðir þar sem gagnatíminn verður uppfærður af stýringum dagsetninga og díma. Eftirfarandi dæmi sýnir eina slíka aðferð.

    ```xpp
    private void setFromDateTime(utcdatetime _value)
        {
            fromDateTime = _value;
        }
    ```

1. Setja upp hegðun hvers gagnatímastjórnborðs og tengja hverja stýringu við formhluta. Eftirfarandi dæmi sýnir hvernig á að setja upp gögn fyrir dagsetningar og tíma frá stjórntækjum. Hægt er að bæta svipuðum kóða fyrir dagsetning-til og tími-til við stýringar (ekki sýnt).

    ```xpp
    /// <summary>
    /// Initializes all date and time controllers, defines their behavior, and connects them with the form parts.
    /// </summary>
    private void initializeDateControlControllers()
    {
        dateFromController = new JmgProductionFloorExecutionDateTimeController();
        dateFromController.setDateControlValueToCallerFormDelegate += eventhandler(this.setFromDateTime);
        dateFromController.parmDateTimeValue(fromDateTime);
    
        timeFromController = new JmgProductionFloorExecutionDateTimeController();
        timeFromController.setDateControlValueToCallerFormDelegate += eventhandler(this.setFromDateTime);
        timeFromController.parmDateTimeValue(fromDateTime);
        
        DateFromFormPart.getPartFormRun().setDateControlController(dateFromController, timeFromController);
        TimeFromFormPart.getPartFormRun().setTimeControlController(timeFromController, dateFromController);
        
        ...

    }
    ```

    Ef þú þarft bara dagastýringu geturðu sleppt uppsetningu tímastýringar og sett upp dagastýringu eins og sýnt er í eftirfarandi dæmi:

    ```xpp
    {
        dateFromController = new JmgProductionFloorExecutionDateTimeController();
        dateFromController.setDateControlValueToCallerFormDelegate += eventhandler(this.setFromDateTime);
        dateFromController.parmDateTimeValue(fromDateTime);
    
        DateFromFormPart.getPartFormRun().setDateControlController(dateFromController, null);
    }
    ```

## <a name="additional-resources"></a>Frekari upplýsingar

- [Hanna keyrsluviðmót framleiðslugólfsins](production-floor-execution-styles.md)
- [Hanna viðmótið fyrir framkvæmd á framleiðslugólfi](production-floor-execution-tabs.md)
