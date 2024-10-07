![Image](https://github.com/user-attachments/assets/b7204414-b8f8-46df-b22f-5482de3e3940)
![Image](https://github.com/user-attachments/assets/f50bb9c8-ee66-474c-816d-b021de1064a0)


apex trigger
trigger consumerTrigger on consumer__c (After insert) {
    if(trigger.isAfter && trigger.isInsert) {
        ConsumerRecord.sendEmailNotification(trigger.new);
    }
}
