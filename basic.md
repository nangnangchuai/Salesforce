- 核心
```
<apex:tab label="Details" name="AccDetails" id="tabdetails">
   <apex:detail relatedList="false" title="true"/>
</apex:tab>



```
- 完整

```
<apex:page standardController="Account" showHeader="true" 
      tabStyle="account" >
   <style>
      .activeTab {background-color: #236FBD; color:white; 
         background-image:none}
      .inactiveTab { background-color: lightgrey; color:black; 
         background-image:none}
   </style>
   <apex:tabPanel switchType="client" selectedTab="tabdetails" 
                  id="AccountTabPanel" tabClass="activeTab" 
                  inactiveTabClass="inactiveTab">   
      
      <apex:tab label="Contacts" name="Contacts" id="tabContact">
         <apex:relatedList subject="{!account}" list="contacts" />
      </apex:tab>
      <apex:tab label="Details" name="clients" id="tabdetails">
         <apex:detail relatedList="false" title="true"/>
      </apex:tab>
      
      
   </apex:tabPanel>
   

</apex:page>
```
地址：https://c.ap8.visual.force.com/apex/hello2?id=0010o00002SdwnGAAR

