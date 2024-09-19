the links :
figma:
https://www.figma.com/design/uGFtV8Jcs5FD52LDU8ESxv/Untitled?node-id=0-1&node-type=canvas&t=0mb4Vv9F04gOYsxK-0

class digram:
https://viewer.diagrams.net/?tags=%7B%7D&lightbox=1&highlight=0000ff&edit=_blank&layers=1&nav=1&title=UML%20Class%20DiagramV.drawio#R%3Cmxfile%3E%3Cdiagram%20name%3D%22Page-1%22%20id%3D%22zDSKSifyWvZF3mbMs29R%22%3EdZHBDsIgDIafhjuDaLzPqRdPO3gmow4Sti4MM%2FTp3QI4yfRE%2Bfr%2FlLaEl50%2FWzGoK0owhFHpCT8Sxgq6o%2FOxkGcge1YE0Foto2gFtX5Bckb60BLGTOgQjdNDDhvse2hcxoS1OOWyO5q86iBa2IC6EWZLb1o6FeghtbXwC%2BhWpcoFjZlOJHEEoxISpy%2FEK8JLi%2BhC1PkSzDK8NJfgO%2F3Jfj5moXc%2FDHOwvj1fsg3x6g0%3D%3C%2Fdiagram%3E%3C%2Fmxfile%3E#%7B%22pageId%22%3A%22zDSKSifyWvZF3mbMs29R%22%7D

use case digram:
https://lucid.app/lucidchart/56ca0f5c-4eb7-4e79-b0f6-14d190e348cf/edit?invitationId=inv_1829aead-4e3d-4d87-a7c0-3da38e9f117b&page=0_0#













PC Centre Flow for Noob website 

  flow Endpoints:


Vendor Adds PC Centre

Vendors can register electronic gaming PC centres, providing details such as location, name, and facilities.
Add PCs to the PC Centre

Vendors can equip their PC centres by adding individual gaming PCs, each with specific configurations and features.
Add Zones to the PC Centre

Vendors can designate areas or zones within the PC centre (e.g., VIP, tournament zones) to enhance the gaming experience.
Vendor Adds Subscription Packages

Vendors create subscription options (e.g., hourly, daily, monthly plans) for players to access the gaming facilities at the PC centre.
Admin Approves the PC Centre

Admins review and approve the vendor's PC centre before it is made available for players, ensuring that it meets the platform's standards.
View Approved PC Centres

Once approved, the PC centres are visible to vendors, players, and admins. Players can browse through the available centres for gaming subscriptions.
View PC Centres by Location and Rating

Players and admins can search for PC centres based on their location or filter by player ratings to find the best gaming experiences nearby.
Player Subscribes to PC Centre

Players can subscribe to the gaming PC centre, selecting from the subscription packages offered by the vendor.
Player Reviews the PC Centre

After using the gaming facilities, players can rate and leave reviews for the PC centre, contributing to its overall rating.
Player Returns Subscription

If a player has used a subscription for less than 25 minutes, they can return it, receiving a refund or cancellation.



1. إضافة المركز من قبل البائع 
   - يمكن للبائعين تسجيل مراكز الألعاب الإلكترونية وتقديم تفاصيل مثل الموقع والاسم والمرافق المتاحة.

2. إضافة أجهزة الكمبيوتر إلى المركز 
   - يقوم البائعون بتجهيز مراكزهم بإضافة أجهزة الكمبيوتر المخصصة للألعاب، مع تحديد كل جهاز حسب مواصفاته وإمكانياته.

3. إضافة المناطق داخل المركز 
   - يمكن للبائعين تخصيص مناطق أو أقسام داخل المركز (مثل مناطق VIP أو مناطق البطولات) لتحسين تجربة اللاعبين.

4. إضافة اشتراكات للمركز 
   - يقوم البائعون بإنشاء باقات اشتراك (مثل الساعات أو اليومي أو الشهري) التي تتيح للاعبين الوصول إلى مرافق الألعاب في المركز.

5. موافقة المدير على المركز 
   - يقوم المديرون بمراجعة والموافقة على المركز المقدم من البائع قبل أن يتم عرضه للاعبين، لضمان توافقه مع معايير المنصة.

6. عرض المراكز المعتمدة
   - بعد الموافقة، تصبح مراكز الألعاب متاحة للبائعين واللاعبين والمديرين، حيث يمكن للاعبين تصفح المراكز المتاحة للاشتراك.

7.  عرض المراكز حسب الموقع والتقييم
   - يمكن للاعبين والمديرين البحث عن مراكز الألعاب بناءً على الموقع أو تصفيتها حسب التقييمات الممنوحة من اللاعبين للحصول على أفضل تجربة لعب.

8. اشتراك اللاعب في المركز  
   - يمكن للاعبين الاشتراك في مركز الألعاب الإلكتروني عن طريق اختيار إحدى الباقات المتاحة من قبل البائع.

9. تقييم اللاعب للمركز 
   - بعد استخدام مرافق الألعاب، يمكن للاعبين تقييم المركز وترك مراجعة، مما يساهم في التقييم الإجمالي للمركز.

10. إرجاع اشتراك اللاعب  
   - إذا استخدم اللاعب الاشتراك لمدة أقل من 25 دقيقة، يمكنه إرجاعه والحصول على استرداد أو إلغاء الاشتراك.





Endpoint and Reltion



Game model:
Reltion  @ManyToMany wit PC model.

Endpoint: Crud 

PC Model: 
Reltion
  @ManyToOne with PC centre model
 @ManyToOne with Zone Model

 Endpoint:Crud
  



  PC centre:
  Reltion : 
  @OneToMany wit PC
  @OneToMany with Zone
  @OneToMany with vendor
  @OneToMany wth subscription
   @OneToMany with review pc centre

   Endpoint: 
   Crud 
   getPcCentresByVendorID
   adminAprovedPcCenter
   getPcCentresByRating
   getPcCentresByRatingRange
   getPcCentreByCentreName
   getPcCentreByLocation
   getApprovedPcCentres
   getAllNotApprovedPcCentre




   review pc centre Model:
     Reltion : 
         @ManyToOne with player
          @ManyToOne with pc centre model
           CRUD
          Endpoint getReviewCentreByPlayerId
          



          SubscribBy Model:
          Reltion :
           @ManyToOne with Subscription model
           @ManyToOne with Player model

           Endpoint:
           CRUD
           getSubscripeByPlayerId
           playerReturnSubscription
           subscribePlayerToSubscription





           Subscription Model :
           Reltion:
           @OneToMany with SubscribBy model
           @ManyToOne with PC centre
           @OneToMany with Zone

           Endpoint:
           CRUD
           getsubscriptionbyPcCentreId




           Vendor Model :
            @OneToOne with User Model
             @OneToMany with PC centre Model

             Endpoint:
             CRUD
             getVendorById


             Zone Model:
             Reltion :

               @OneToMany with PC model
                  @ManyToOne with subscription model
                     @ManyToOne with PC centre

                     Endpoint:
                    CRUD
                    getZoneByPcCentre
                    changeZoneStatus


                  






   


