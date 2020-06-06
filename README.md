#62wir31
RoomandRoommatematching
└───RoomandRoommatematching
    ├───bin
    │   └───Debug
    │       ├───netcoreapp2.1
    │       └───netcoreapp3.1
    │           ├───cs
    │           ├───de
    │           ├───es
    │           ├───fr
    │           ├───it
    │           ├───ja
    │           ├───ko
    │           ├───pl
    │           ├───Properties
    │           ├───pt-BR
    │           ├───ru
    │           ├───runtimes
    │           │   ├───unix
    │           │   │   └───lib
    │           │   │       └───netcoreapp2.1
    │           │   ├───win
    │           │   │   └───lib
    │           │   │       └───netcoreapp2.1
    │           │   ├───win-arm64
    │           │   │   └───native
    │           │   ├───win-x64
    │           │   │   └───native
    │           │   └───win-x86
    │           │       └───native
    │           ├───tr
    │           ├───zh-Hans
    │           └───zh-Hant
    ├───Controllers
    ├───Models
    ├───obj
    │   └───Debug
    │       ├───netcoreapp2.1
    │       └───netcoreapp3.1
    │           ├───Razor
    │           │   └───Views
    │           │       ├───Admin
    │           │       ├───Home
    │           │       ├───Invitation
    │           │       ├───JoinRoommate
    │           │       ├───Room
    │           │       ├───Roommate
    │           │       └───Shared
    │           │           └───Components
    │           │               └───UserView
    │           └───staticwebassets
    ├───Properties
    │   └───PublishProfiles
    ├───Views
    │   ├───Admin
    │   ├───Home
    │   ├───Invitation
    │   ├───JoinRoommate
    │   ├───Room
    │   ├───Roommate
    │   └───Shared
    │       └───Components
    │           └───UserView
    └───wwwroot
        ├───css
        ├───fonts
        │   ├───Dancing_Script
        │   │   └───static
        │   ├───Erasdemi
        │   └───Kanit
        ├───images
        │   ├───dormitory
        │   ├───joinroommate
        │   ├───map
        │   ├───room
        │   └───roommate
        ├───js
        └───lib
            ├───bootstrap
            │   └───dist
            │       ├───css
            │       └───js
            ├───jquery
            │   └───dist
            ├───jquery-validation
            │   └───dist
            └───jquery-validation-unobtrusive

วิธีการติดตั้ง
1.ติดตั้ง Visual Studio 2019 (วิธีการติดตั้ง https://youtu.be/0P2uQuTrgtg)
2.ติดตั้ง SQL Server Management Studio 2018 (วิธีการติดตั้ง https://youtu.be/BGbBP-CAeXk)
3.นำไฟล์ ROOMROOMMATE.bak ไปไว้ใน path C:\Program Files\Microsoft SQL Server\MSSQL14.SQLEXPRESS\MSSQL\Backup

หลังจากทำการติดตั้งตัวโปรแกรมทั้งสองโปรแกรมเสร็จเรียบร้อยแล้ว ให้ทำการลงตัวไฟล์ดาต้าเบสที่แนบไว้ให้ใน โฟลเดอร์ /src ไฟล์ชื่อว่า ROOMROOMMATE.bak

วิธีการติดตั้ง/ลงไฟล์ดาต้าเบสแบบละเอียดในโปรแกรม SQL Server Management Studio 2018
- เปิดตัวโปรแกรม SQL Server Management Studio 2018 ขึ้นมา
- กดคลิกขวาที่โฟลเดอร์ Database ที่อยู่บนแถบซ้ายมือ > กด Restore Database
- จากนั้นจะแสดงหน้าต่างขึ้นมา ให้กด Device > แล้วกดเลือกไฟล์โดยกด Add
- แล้วไปที่ path C:\Program Files\Microsoft SQL Server\MSSQL14.SQLEXPRESS\MSSQL\Backup และ กดเลือกไฟล์ ROOMROOMMATE.bak
- จากนั้นดูที่เมนูด้านซ้าย 'Select a page' ให้คลิกที่เมนูที่ชื่อว่า Options
- ให้ทำการเลือก Overwrite the existing database (WITH REPLACE) แล้วกด OK 

วิธีการลบไฟล์ roommate security ใน Database ที่ได้ Restore ไป เพื่อเข้าสู่ระบบ
- เลือกไฟล์ดาต้าเบสหลัก ROOMROOMMATE > เลือกโฟลเดอร์ security > เลือกโฟลเดอร์ user > คลิกขวาที่ไฟล์ roommate แล้วเลือก Delete แล้วกด OK
- เลือกโฟลเดอร์หลัก Security > คลิกเข้าไปในไฟลเดอร์ Logins > ดับเบิ้ลคลิกที่ไฟล์ดาต้าเบสชื่อว่า roommate > ช่องด้านบนให้คลิกเลือกชื่อดาต้าเบส ROOMROOMMATE > ดูช่องข้างล่างให้เลือก db_owner แล้วกด OK เป็นอันเสร็จสิ้น 

การเปิดตัวโปรแกรม
- ให้ทำการแตกไฟล์ RoomandRoommateMatching.zip ก่อน
- หลังจากนั้นในไฟล์ .zip จะมีโฟลเดอร์ กับ ไฟล์ที่เป็นตัวโปรแกรมชื่อว่า RoomandRoommateMatching
- ให้ทำการกดเปิดไฟล์ที่ชื่อว่า RoomandRoommateMatching 
- หลังจากเปิดแล้วให้ทำการคลิก IIS Express ที่อยู่บนบาร์ด้านบน หรือสามารถกดปุ่ม F5 เพื่อรันตัวโปรแกรมได้