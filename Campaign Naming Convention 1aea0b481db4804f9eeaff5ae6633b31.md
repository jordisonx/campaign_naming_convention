# Campaign Naming Convention

- **List of Parameters**
    - `{gameCode}`: MOC, CUE, BLJ, etc
    - `{OS}`: Android, IOS, etc
    - `{Country|GEO-Tier}`: Single country, or single GEO Tier(WW, T1, T2, Tx, etc), or multiple countries
        - In case of multiple countries: Should be separated by dashes(’-’) and max. 5 countries displayed at a time.
    - `{optimizationType}[IF_AEO:eventName]`: What optimization type does the campaign use? VO-IAA, VO-Hybrid, VO-IAP, AEO, etc
        - If the optimization type is AEO, the event being optimized for should be noted in brackets.
        - If the optimization type is VO, the specific purchase event will be shown ***if relevant.*** If not, no brackets
            - Example: VO-IAA[ad_impression], VO-IAA[ad_revenue], VO-IAP[non-consumable]
        - If optimization type is Retargeting, the retargeted segment should be noted. PU, NPU, ,etc
        - Test campaigns will not be noted under this parameter; but will be determined as Test campaigns if their name includes ‘Test’ anywhere in the name
    - `{optimizationWindow}`: D0, D7, D28, etc
    - `{campaignModel}`: Notes the possible campaign types(mostly for FB and TT); Manual campaign, Advantage+, Smart+, ADC, etc
    - `{attributionModel}`: Facebook[IOS]-specific parameter. Notes the attribution model used in the campaign. SKAN or AEM
    - `{Lookalike}`: Name of the lookalike audience; won’t be used if no Lookalikes used
    - `{CustomNotes}`: Anything else you’d like to include in the campaign name. No structure or limits are set here.
- **Parameter-Value Pairs**
    - `{gameCode}`
        - Valid Values: Any available three-letter(uppercase) Voodoo game code
    - `{OS}`
        - Valid Values: Android, IOS, CTV, Other
    - `{Country|GEO-Tier}`
        - Valid Values: Any two letter(uppercase) country codes(including WW), T1, T2, T3, T4, RoW
    - `{optimizationType}[IF_AEO:eventName]`
        - Valid Values: Install, AEO[{eventName}], VO-IAA, VO-IAP, VO-Hybrid, Retargeting, Search, Rewarded
    - `{optimizationWindow}`
        - Valid Values: D0, D1, D3, D7, D14, D28
            - Open to expansion
    - `{campaignModel}`
        - Valid Values: Manual, AdvP, SPC, ADC,
    - `{attributionModel}`
        - Valid Values: SKAN, AEM
    - `{Lookalike}`
        - Custom field w/ character limit(exact limit TBD)
    - `{CustomNotes}`
        - Custom field w/o limits
- **Fields to be enabled on Tableau Dashboards**
    - ⚠️ Each row listed below should be a separate field
    - Optimization Type
    - Optimization Window
    - Channel Type
        - Ad Network, Social, Search, Rewarded, etc
    - Campaign Model
    - Attribution Model
- **Naming Conventions per Channel**
    
    ### :facebook_logo_-square-: Facebook
    
    - Android
        - `{gameCode}_{OS}_{Country|GEO-Tier}_{optimizationType}[IF_AEO:eventName]_{optimizationWindow}_{campaignModel}_{lookalike}_{customNotes}`
            - 💡**Example**: MOC_Android_T1_VO-IAA_D7_AdvP
            - 💡**Example**: MOC_Android_US_AEO[Purchase]_D7_Manual
    - IOS
        - `{gameCode}_{OS}_{Country|GEO-Tier}_{optimizationType}[IF_AEO:eventName]_{optimizationWindow}_{campaignModel}_{attributionModel}_{lookalike}_{customNotes}`
            - 💡**Example**: CUE_IOS_US_VO-Hybird_D7_Manual_AEM
    
    ### :tiktok: TikTok
    
    - Android & IOS
        - `{gameCode}_{OS}_{Country|GEO-Tier}_{optimizationType}[IF_AEO:eventName]_{optimizationWindow}_{campaignModel}_{lookalike}_{customNotes}`
            - 💡**Example**: BBT_Android_T1_VO-IAA_D0_SPC_Pangle
    
    ## 🔀 Every Other Channel
    
    - Android & IOS
        - `{gameCode}_{OS}_{Country|GEO-Tier}_{optimizationType}[IF_AEO:eventName]_{optimizationWindow}_{customNotes}`
            - **💡Example:** MOC_Android_US_VO-IAA_D3_[NoMid_FS30_Win_Loss]
            - **💡Example:** BLJ_IOS_WW_VO-IAA_D28
            - **💡Example:** MOC_Android_US_Retargeting[PU]_D0
- **BeachBum Campaign Naming Convention**
    
    ![Screenshot 2025-03-11 at 18.00.30.png](Campaign%20Naming%20Convention%201aea0b481db4804f9eeaff5ae6633b31/Screenshot_2025-03-11_at_18.00.30.png)