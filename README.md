# plantuml-office
Office Icons for PlantUML

## Usage
There are sprites (*.puml) and colored png icons available. Be aware that the sprites are all only monchrome even if they have a color in their name (due to automatically generating the files). You can either color the sprites with the macro (see examples below) or directly use the fully colored pngs. See the following examples on how to use the sprites, the pngs and the macros.

Example of usage:
```
@startuml
!include <font-awesome/common>

!define ICONURL https://raw.githubusercontent.com/Roemer/plantuml-office/master/office2014
!includeurl ICONURL/Servers/database_server.puml
!includeurl ICONURL/Servers/application_server.puml
!includeurl ICONURL/Concepts/firewall_orange.puml
!includeurl ICONURL/Clouds/cloud_disaster_red.puml

title Office Icons Example

package "Sprites" {
    OFF_DATABASE_SERVER(db,DB)
    OFF_APPLICATION_SERVER(app,App-Server)
    OFF_FIREWALL_ORANGE(fw,Firewall)
    OFF_CLOUD_DISASTER_RED(cloud,Cloud)
    db <-> app
    app <--> fw
    fw <.left.> cloud
}

package "Images" {
    rectangle "<img:https://raw.githubusercontent.com/Roemer/plantuml-office/master/office2014/Servers/database_server.png>\r DB" as db2
    rectangle "<img:https://raw.githubusercontent.com/Roemer/plantuml-office/master/office2014/Servers/application_server.png>\r App-Server" as app2
    rectangle "<img:https://raw.githubusercontent.com/Roemer/plantuml-office/master/office2014/Concepts/firewall_orange.png>\r Firewall" as fw2
    rectangle "<img:https://raw.githubusercontent.com/Roemer/plantuml-office/master/office2014/Clouds/cloud_disaster_red.png>\r Cloud" as cloud2
    db2 <-> app2
    app2 <--> fw2
    fw2 <.left.> cloud2
}

@enduml
```

This example renders the following image:

![Example](http://www.plantuml.com/plantuml/png/jLF1Yjim4BtxAxGvfP14RUXf2M6Ts2c642zsjhqKZ2AFlQAo92IvBfJ-UnMfJaeXxQNnPJoZzppleUSdOucsVSUZ1oOexsj0gqOAEoS36Da1fhBhf5X7qKCD3HE0icr-U2dswDLQPHunrcHOjCo-zgVUWAQE2y8k70qN4ZhGM74YpXlcicaO1TmHOzquTCktxzvVLlUQZv_79UYle0skYIKdOg0oVh1GGUjj0b6ACqeia-AVdAqK59Grk64Q1i9v9JKHBVo5mMLV6qpFfQgPyLug3NMWH9PP3YZttb16fJ0e_KOwnI6A5A5VI0jeKYhDB9W9-XuXz-IxNPN4ntWJbsbLfiN7j9ZMfrcoUNCvZf-VzzasFcRvOKGudxDOgNdmVONkiYBz5E_tLLx4Xm_fj1bckr_khg3jFdz9gYGhu_AO5bMH9bDlQURz1LnzGglv6hazldNLzMxG3Bvl1hHQS6ZiOeqyD_hncyMiS-NYK0ErHBJS7QnOrpx-l-pSpebervyrIZOJH8ppiho_aDlv2rgkj-KrEU3THTqEU90q9iCBQeRxwxdz-mH17k3LU4mGv6vlZA8V-9SnZ67YwXznN9xp-0IYTe9-0W00)

Further example:
```
@startuml
!include <font-awesome/common>

!define ICONURL https://raw.githubusercontent.com/Roemer/plantuml-office/master/office2014
!includeurl ICONURL/Servers/database_server.puml
!includeurl ICONURL/Servers/application_server.puml
!includeurl ICONURL/Concepts/firewall_orange.puml
!includeurl ICONURL/Clouds/cloud_disaster_red.puml

' Used to center the label under the images
skinparam defaultTextAlignment center

title Extended Office Icons Example

package "Use sprite directly" {
    [Some <$cloud_disaster_red> object]
}

package "Different makro usages" {
    OFF_CLOUD_DISASTER_RED(cloud1)
    OFF_CLOUD_DISASTER_RED(cloud2,Default with text)
    OFF_CLOUD_DISASTER_RED(cloud3,Other shape,Folder)
    OFF_CLOUD_DISASTER_RED(cloud4,Even another shape,Database)
    OFF_CLOUD_DISASTER_RED(cloud5,Colored,Rectangle, red)
    OFF_CLOUD_DISASTER_RED(cloud6,Colored background) #red
}
@enduml
```

This example renders the following image:

![Example](http://www.plantuml.com/plantuml/png/XP9RQzj048NVzrTCqa8RKAmcJVjGGaYmR3246kpuAHGnrexihVUox8xYbDB_teal9L28z2BsQBypciEvpOo9EsVLYV6DxJJ1THiyd-EMSd1KDi6vu6-KEj7K6aym6Kw_BsRti6QE-LjP9jmELeRNtRBBb1fXoVD0i78Mo54geqN_Ck4yjArfg7IOMUJzwVBJnTM_qLsoH_joJkc9KYurCYunKvrtmY2Aqvi0ncXDWso2xsM6mJSKEPUjIRH5Q-kGqA_e3SA6JkUoUNdLskJTBdKYlKVK1rXaqi016lBo2NXDO7595Zgl3sVZS4LPvOtn4HCwa6Yni_n0ptndpSexOGy6Ih5XIp1wPX833TDTRZ2HfBEewA8bfI8s6p65KnaFEIR31DeaQjZ-EeNV2kHvd0T7SFt-_v-_WR3yANT_g3-lh2hJjfJ8CpZSf01T5ZaVtQRZSJsydowgkfhCx-OFeraz6rKVT-ONPxrNBejglpHifJp0ide_zBcOIdu9yXeZ5UDW9T5-wgeOFP47zE4LN1rwrOz_AOR11acfc4b4KWzB1SYnd_nw964fcQvIa0gSmJiH9ETRybegynS0)

## Icon Index
Category | Macro | Image | Url
--- | --- | --- | ---
Clouds | OFF_AZURE | ![azure](/office2014/Clouds/azure.png?raw=true) | Clouds/azure.puml
Clouds | OFF_CLOUD | ![cloud](/office2014/Clouds/cloud.png?raw=true) | Clouds/cloud.puml
Clouds | OFF_CLOUD_DISASTER | ![cloud_disaster](/office2014/Clouds/cloud_disaster.png?raw=true) | Clouds/cloud_disaster.puml
Clouds | OFF_CLOUD_DISASTER_RED | ![cloud_disaster_red](/office2014/Clouds/cloud_disaster_red.png?raw=true) | Clouds/cloud_disaster_red.puml
Clouds | OFF_CLOUD_EXCHANGE_ONLINE | ![cloud_exchange_online](/office2014/Clouds/cloud_exchange_online.png?raw=true) | Clouds/cloud_exchange_online.puml
Clouds | OFF_CLOUD_SERVICE_REQUEST | ![cloud_service_request](/office2014/Clouds/cloud_service_request.png?raw=true) | Clouds/cloud_service_request.puml
Clouds | OFF_CLOUD_SHAREPOINT_ONLINE | ![cloud_sharepoint_online](/office2014/Clouds/cloud_sharepoint_online.png?raw=true) | Clouds/cloud_sharepoint_online.puml
Clouds | OFF_OFFICE_365_CLOUD | ![office_365_cloud](/office2014/Clouds/office_365_cloud.png?raw=true) | Clouds/office_365_cloud.puml
Clouds | OFF_ONLINE_BACKUP | ![online_backup](/office2014/Clouds/online_backup.png?raw=true) | Clouds/online_backup.puml
Clouds | OFF_ONLINE_USER | ![online_user](/office2014/Clouds/online_user.png?raw=true) | Clouds/online_user.puml
Clouds | OFF_PRIVATE_CLOUD | ![private_cloud](/office2014/Clouds/private_cloud.png?raw=true) | Clouds/private_cloud.puml
Clouds | OFF_PUBLIC_CLOUD | ![public_cloud](/office2014/Clouds/public_cloud.png?raw=true) | Clouds/public_cloud.puml
Clouds | OFF_PUBLIC_IM_CLOUD_SERVICE | ![public_im_cloud_service](/office2014/Clouds/public_im_cloud_service.png?raw=true) | Clouds/public_im_cloud_service.puml
Communications | OFF_3RD_PARTY_CALL_CENTER_SOLUTION | ![3rd_party_call_center_solution](/office2014/Communications/3rd_party_call_center_solution.png?raw=true) | Communications/3rd_party_call_center_solution.puml
Communications | OFF_3RD_PARTY_INTEGRATION | ![3rd_party_integration](/office2014/Communications/3rd_party_integration.png?raw=true) | Communications/3rd_party_integration.puml
Communications | OFF_3RD_PARTY_SERVICE | ![3rd_party_service](/office2014/Communications/3rd_party_service.png?raw=true) | Communications/3rd_party_service.puml
Communications | OFF_APPLICATION_SHARING_WORKLOAD | ![application_sharing_workload](/office2014/Communications/application_sharing_workload.png?raw=true) | Communications/application_sharing_workload.puml
Communications | OFF_AUDIO_CONFERENCING_APPLICATION | ![audio_conferencing_application](/office2014/Communications/audio_conferencing_application.png?raw=true) | Communications/audio_conferencing_application.puml
Communications | OFF_CENTRAL_MANAGEMENT_SERVICE | ![central_management_service](/office2014/Communications/central_management_service.png?raw=true) | Communications/central_management_service.puml
Communications | OFF_CHAT_ROOM | ![chat_room](/office2014/Communications/chat_room.png?raw=true) | Communications/chat_room.puml
Communications | OFF_CONFERENCE_ANNOUNCEMENT_SERVICE | ![conference_announcement_service](/office2014/Communications/conference_announcement_service.png?raw=true) | Communications/conference_announcement_service.puml
Communications | OFF_DISCONNECTED_MAILBOX | ![disconnected_mailbox](/office2014/Communications/disconnected_mailbox.png?raw=true) | Communications/disconnected_mailbox.puml
Communications | OFF_DISCOVERY_SEARCH_MAILBOX | ![discovery_search_mailbox](/office2014/Communications/discovery_search_mailbox.png?raw=true) | Communications/discovery_search_mailbox.puml
Communications | OFF_DYNAMIC_DISTRIBUTION_GROUP | ![dynamic_distribution_group](/office2014/Communications/dynamic_distribution_group.png?raw=true) | Communications/dynamic_distribution_group.puml
Communications | OFF_EDGE_SUBSCRIPTION | ![edge_subscription](/office2014/Communications/edge_subscription.png?raw=true) | Communications/edge_subscription.puml
Communications | OFF_EMAIL_WORKLOAD | ![email_workload](/office2014/Communications/email_workload.png?raw=true) | Communications/email_workload.puml
Communications | OFF_EQUIPMENT_MAILBOX | ![equipment_mailbox](/office2014/Communications/equipment_mailbox.png?raw=true) | Communications/equipment_mailbox.puml
Communications | OFF_EXCHANGE_ACTIVE_SYNC | ![exchange_active_sync](/office2014/Communications/exchange_active_sync.png?raw=true) | Communications/exchange_active_sync.puml
Communications | OFF_EXCHANGE_ACTIVE_SYNC_BLUE | ![exchange_active_sync_blue](/office2014/Communications/exchange_active_sync_blue.png?raw=true) | Communications/exchange_active_sync_blue.puml
Communications | OFF_FAX_PARTNER | ![fax_partner](/office2014/Communications/fax_partner.png?raw=true) | Communications/fax_partner.puml
Communications | OFF_GLOBAL_ADDRESS_LIST | ![global_address_list](/office2014/Communications/global_address_list.png?raw=true) | Communications/global_address_list.puml
Communications | OFF_HYBRID_VOIP_GATEWAY | ![hybrid_voip_gateway](/office2014/Communications/hybrid_voip_gateway.png?raw=true) | Communications/hybrid_voip_gateway.puml
Communications | OFF_IM_WORKLOAD | ![im_workload](/office2014/Communications/im_workload.png?raw=true) | Communications/im_workload.puml
Communications | OFF_JOURNALING_RULE | ![journaling_rule](/office2014/Communications/journaling_rule.png?raw=true) | Communications/journaling_rule.puml
Communications | OFF_LOCAL_MOVE_REQUEST | ![local_move_request](/office2014/Communications/local_move_request.png?raw=true) | Communications/local_move_request.puml
Communications | OFF_LYNC_CONTROL_PANEL | ![lync_control_panel](/office2014/Communications/lync_control_panel.png?raw=true) | Communications/lync_control_panel.puml
Communications | OFF_LYNC_PHONE_EDITION | ![lync_phone_edition](/office2014/Communications/lync_phone_edition.png?raw=true) | Communications/lync_phone_edition.puml
Communications | OFF_LYNC_ROOM_SYSTEM | ![lync_room_system](/office2014/Communications/lync_room_system.png?raw=true) | Communications/lync_room_system.puml
Communications | OFF_LYNC_SERVER_MANAGEMENT_TOOL | ![lync_server_management_tool](/office2014/Communications/lync_server_management_tool.png?raw=true) | Communications/lync_server_management_tool.puml
Communications | OFF_LYNC_STORAGE_SERVICE | ![lync_storage_service](/office2014/Communications/lync_storage_service.png?raw=true) | Communications/lync_storage_service.puml
Communications | OFF_LYNC_WEB_APP_CLIENT | ![lync_web_app_client](/office2014/Communications/lync_web_app_client.png?raw=true) | Communications/lync_web_app_client.puml
Communications | OFF_MAILBOX_ASSISTANT | ![mailbox_assistant](/office2014/Communications/mailbox_assistant.png?raw=true) | Communications/mailbox_assistant.puml
Communications | OFF_MAIL_ENABLED_PUBLIC_FOLDER | ![mail_enabled_public_folder](/office2014/Communications/mail_enabled_public_folder.png?raw=true) | Communications/mail_enabled_public_folder.puml
Communications | OFF_MESSAGES_QUEUED | ![messages_queued](/office2014/Communications/messages_queued.png?raw=true) | Communications/messages_queued.puml
Communications | OFF_OFFLINE_ADDRESS_BOOK | ![offline_address_book](/office2014/Communications/offline_address_book.png?raw=true) | Communications/offline_address_book.puml
Communications | OFF_PERSONAL_ARCHIVE_MAILBOX | ![personal_archive_mailbox](/office2014/Communications/personal_archive_mailbox.png?raw=true) | Communications/personal_archive_mailbox.puml
Communications | OFF_PUBLIC_IM_CLOUD_SERVICE | ![public_im_cloud_service](/office2014/Communications/public_im_cloud_service.png?raw=true) | Communications/public_im_cloud_service.puml
Communications | OFF_PUSH_NOTIFICATION_SERVICE | ![push_notification_service](/office2014/Communications/push_notification_service.png?raw=true) | Communications/push_notification_service.puml
Communications | OFF_QUEUE_VIEWER | ![queue_viewer](/office2014/Communications/queue_viewer.png?raw=true) | Communications/queue_viewer.puml
Communications | OFF_REMOTE_MAILBOX | ![remote_mailbox](/office2014/Communications/remote_mailbox.png?raw=true) | Communications/remote_mailbox.puml
Communications | OFF_REMOTE_MOVE_REQUEST | ![remote_move_request](/office2014/Communications/remote_move_request.png?raw=true) | Communications/remote_move_request.puml
Communications | OFF_RESPONSE_GROUP | ![response_group](/office2014/Communications/response_group.png?raw=true) | Communications/response_group.puml
Communications | OFF_RESPONSE_GROUP_SERVICE | ![response_group_service](/office2014/Communications/response_group_service.png?raw=true) | Communications/response_group_service.puml
Communications | OFF_ROOM_MAILBOX | ![room_mailbox](/office2014/Communications/room_mailbox.png?raw=true) | Communications/room_mailbox.puml
Communications | OFF_SHARED_MAILBOX | ![shared_mailbox](/office2014/Communications/shared_mailbox.png?raw=true) | Communications/shared_mailbox.puml
Communications | OFF_SIP_URI_UM_DIAL_PLAN | ![sip_uri_um_dial_plan](/office2014/Communications/sip_uri_um_dial_plan.png?raw=true) | Communications/sip_uri_um_dial_plan.puml
Communications | OFF_SITE_MAILBOX | ![site_mailbox](/office2014/Communications/site_mailbox.png?raw=true) | Communications/site_mailbox.puml
Communications | OFF_SKYPE_FOR_BUSINESS_CONTROL_PANEL | ![skype_for_business_control_panel](/office2014/Communications/skype_for_business_control_panel.png?raw=true) | Communications/skype_for_business_control_panel.puml
Communications | OFF_SKYPE_FOR_BUSINESS_PHONE_EDITION | ![skype_for_business_phone_edition](/office2014/Communications/skype_for_business_phone_edition.png?raw=true) | Communications/skype_for_business_phone_edition.puml
Communications | OFF_SKYPE_FOR_BUSINESS_ROOM_SYSTEM | ![skype_for_business_room_system](/office2014/Communications/skype_for_business_room_system.png?raw=true) | Communications/skype_for_business_room_system.puml
Communications | OFF_SKYPE_FOR_BUSINESS_SERVER_MANAGEMENT_TOOL | ![skype_for_business_server_management_tool](/office2014/Communications/skype_for_business_server_management_tool.png?raw=true) | Communications/skype_for_business_server_management_tool.puml
Communications | OFF_SKYPE_FOR_BUSINESS_STORAGE_SERVICE | ![skype_for_business_storage_service](/office2014/Communications/skype_for_business_storage_service.png?raw=true) | Communications/skype_for_business_storage_service.puml
Communications | OFF_SKYPE_FOR_BUSINESS_WEB_APP_CLIENT | ![skype_for_business_web_app_client](/office2014/Communications/skype_for_business_web_app_client.png?raw=true) | Communications/skype_for_business_web_app_client.puml
Communications | OFF_SMS_GATEWAY | ![sms_gateway](/office2014/Communications/sms_gateway.png?raw=true) | Communications/sms_gateway.puml
Communications | OFF_SMTP_CONNECTOR | ![smtp_connector](/office2014/Communications/smtp_connector.png?raw=true) | Communications/smtp_connector.puml
Communications | OFF_SYSTEM_MAILBOX | ![system_mailbox](/office2014/Communications/system_mailbox.png?raw=true) | Communications/system_mailbox.puml
Communications | OFF_TDM_PBX | ![tdm_pbx](/office2014/Communications/tdm_pbx.png?raw=true) | Communications/tdm_pbx.puml
Communications | OFF_TELEPHONE_EXTENSION_DIAL_PLAN | ![telephone_extension_dial_plan](/office2014/Communications/telephone_extension_dial_plan.png?raw=true) | Communications/telephone_extension_dial_plan.puml
Communications | OFF_TRANSPORT_RULE | ![transport_rule](/office2014/Communications/transport_rule.png?raw=true) | Communications/transport_rule.puml
Communications | OFF_UCMA_APPLICATION | ![ucma_application](/office2014/Communications/ucma_application.png?raw=true) | Communications/ucma_application.puml
Communications | OFF_UCWA_APPLICATION | ![ucwa_application](/office2014/Communications/ucwa_application.png?raw=true) | Communications/ucwa_application.puml
Communications | OFF_UM_AUTO_ATTENDANT | ![um_auto_attendant](/office2014/Communications/um_auto_attendant.png?raw=true) | Communications/um_auto_attendant.puml
Communications | OFF_UM_DIAL_PLAN_E164 | ![um_dial_plan_e164](/office2014/Communications/um_dial_plan_e164.png?raw=true) | Communications/um_dial_plan_e164.puml
Communications | OFF_UM_DIAL_PLAN_SECONDARY | ![um_dial_plan_secondary](/office2014/Communications/um_dial_plan_secondary.png?raw=true) | Communications/um_dial_plan_secondary.puml
Communications | OFF_UM_ENABLED_MAILBOX | ![um_enabled_mailbox](/office2014/Communications/um_enabled_mailbox.png?raw=true) | Communications/um_enabled_mailbox.puml
Communications | OFF_UM_HUNT_GROUP | ![um_hunt_group](/office2014/Communications/um_hunt_group.png?raw=true) | Communications/um_hunt_group.puml
Communications | OFF_UM_IP_GATEWAY | ![um_ip_gateway](/office2014/Communications/um_ip_gateway.png?raw=true) | Communications/um_ip_gateway.puml
Communications | OFF_USER_MAILBOX | ![user_mailbox](/office2014/Communications/user_mailbox.png?raw=true) | Communications/user_mailbox.puml
Communications | OFF_VIDEO_WORKLOAD | ![video_workload](/office2014/Communications/video_workload.png?raw=true) | Communications/video_workload.puml
Communications | OFF_VOICE_MAIL_PREVIEW_PARTNER | ![voice_mail_preview_partner](/office2014/Communications/voice_mail_preview_partner.png?raw=true) | Communications/voice_mail_preview_partner.puml
Communications | OFF_VOICE_WORKLOAD | ![voice_workload](/office2014/Communications/voice_workload.png?raw=true) | Communications/voice_workload.puml
Communications | OFF_VOIP_GATEWAY | ![voip_gateway](/office2014/Communications/voip_gateway.png?raw=true) | Communications/voip_gateway.puml
Communications | OFF_WATCHER_NODE | ![watcher_node](/office2014/Communications/watcher_node.png?raw=true) | Communications/watcher_node.puml
Communications | OFF_XMPP_SERVICE | ![xmpp_service](/office2014/Communications/xmpp_service.png?raw=true) | Communications/xmpp_service.puml
Concepts | OFF_ADDRESS_BOOK | ![address_book](/office2014/Concepts/address_book.png?raw=true) | Concepts/address_book.puml
Concepts | OFF_ANTI_SPAM | ![anti_spam](/office2014/Concepts/anti_spam.png?raw=true) | Concepts/anti_spam.puml
Concepts | OFF_APPLICATION_ANDROID | ![application_android](/office2014/Concepts/application_android.png?raw=true) | Concepts/application_android.puml
Concepts | OFF_APPLICATION_GENERIC | ![application_generic](/office2014/Concepts/application_generic.png?raw=true) | Concepts/application_generic.puml
Concepts | OFF_APPLICATION_HYBRID | ![application_hybrid](/office2014/Concepts/application_hybrid.png?raw=true) | Concepts/application_hybrid.puml
Concepts | OFF_APPLICATION_IOS | ![application_ios](/office2014/Concepts/application_ios.png?raw=true) | Concepts/application_ios.puml
Concepts | OFF_APPLICATION_WEB | ![application_web](/office2014/Concepts/application_web.png?raw=true) | Concepts/application_web.puml
Concepts | OFF_APPLICATION_WINDOWS | ![application_windows](/office2014/Concepts/application_windows.png?raw=true) | Concepts/application_windows.puml
Concepts | OFF_APP_FOR_OFFICE | ![app_for_office](/office2014/Concepts/app_for_office.png?raw=true) | Concepts/app_for_office.puml
Concepts | OFF_APP_FOR_SHAREPOINT | ![app_for_sharepoint](/office2014/Concepts/app_for_sharepoint.png?raw=true) | Concepts/app_for_sharepoint.puml
Concepts | OFF_APP_PART | ![app_part](/office2014/Concepts/app_part.png?raw=true) | Concepts/app_part.puml
Concepts | OFF_ARCHIVE | ![archive](/office2014/Concepts/archive.png?raw=true) | Concepts/archive.puml
Concepts | OFF_ATTACHMENT | ![attachment](/office2014/Concepts/attachment.png?raw=true) | Concepts/attachment.puml
Concepts | OFF_BACKUP_LOCAL | ![backup_local](/office2014/Concepts/backup_local.png?raw=true) | Concepts/backup_local.puml
Concepts | OFF_BACKUP_ONLINE | ![backup_online](/office2014/Concepts/backup_online.png?raw=true) | Concepts/backup_online.puml
Concepts | OFF_BANDWIDTH | ![bandwidth](/office2014/Concepts/bandwidth.png?raw=true) | Concepts/bandwidth.puml
Concepts | OFF_BANDWIDTH_CALCULATOR | ![bandwidth_calculator](/office2014/Concepts/bandwidth_calculator.png?raw=true) | Concepts/bandwidth_calculator.puml
Concepts | OFF_BEST_PRACTICES | ![best_practices](/office2014/Concepts/best_practices.png?raw=true) | Concepts/best_practices.puml
Concepts | OFF_BOOK_JOURNAL | ![book_journal](/office2014/Concepts/book_journal.png?raw=true) | Concepts/book_journal.puml
Concepts | OFF_CALCULATOR | ![calculator](/office2014/Concepts/calculator.png?raw=true) | Concepts/calculator.puml
Concepts | OFF_CALENDAR | ![calendar](/office2014/Concepts/calendar.png?raw=true) | Concepts/calendar.puml
Concepts | OFF_CLIPBOARD | ![clipboard](/office2014/Concepts/clipboard.png?raw=true) | Concepts/clipboard.puml
Concepts | OFF_CLOCK | ![clock](/office2014/Concepts/clock.png?raw=true) | Concepts/clock.puml
Concepts | OFF_COLUMN | ![column](/office2014/Concepts/column.png?raw=true) | Concepts/column.puml
Concepts | OFF_CONNECTOR | ![connector](/office2014/Concepts/connector.png?raw=true) | Concepts/connector.puml
Concepts | OFF_CONTACTS | ![contacts](/office2014/Concepts/contacts.png?raw=true) | Concepts/contacts.puml
Concepts | OFF_CONTENT_TYPE | ![content_type](/office2014/Concepts/content_type.png?raw=true) | Concepts/content_type.puml
Concepts | OFF_CREDIT_CARD | ![credit_card](/office2014/Concepts/credit_card.png?raw=true) | Concepts/credit_card.puml
Concepts | OFF_DOCUMENT | ![document](/office2014/Concepts/document.png?raw=true) | Concepts/document.puml
Concepts | OFF_DOCUMENTS | ![documents](/office2014/Concepts/documents.png?raw=true) | Concepts/documents.puml
Concepts | OFF_DOCUMENTS_SHARED | ![documents_shared](/office2014/Concepts/documents_shared.png?raw=true) | Concepts/documents_shared.puml
Concepts | OFF_DOCUMENT_BLANK | ![document_blank](/office2014/Concepts/document_blank.png?raw=true) | Concepts/document_blank.puml
Concepts | OFF_DOCUMENT_SHARED | ![document_shared](/office2014/Concepts/document_shared.png?raw=true) | Concepts/document_shared.puml
Concepts | OFF_DOWNLOAD | ![download](/office2014/Concepts/download.png?raw=true) | Concepts/download.puml
Concepts | OFF_EMAIL | ![email](/office2014/Concepts/email.png?raw=true) | Concepts/email.puml
Concepts | OFF_EMAIL_APPROVED | ![email_approved](/office2014/Concepts/email_approved.png?raw=true) | Concepts/email_approved.puml
Concepts | OFF_EMAIL_EXPIRED | ![email_expired](/office2014/Concepts/email_expired.png?raw=true) | Concepts/email_expired.puml
Concepts | OFF_EMAIL_REJECTED | ![email_rejected](/office2014/Concepts/email_rejected.png?raw=true) | Concepts/email_rejected.puml
Concepts | OFF_FILE_KEY | ![file_key](/office2014/Concepts/file_key.png?raw=true) | Concepts/file_key.puml
Concepts | OFF_FIREWALL | ![firewall](/office2014/Concepts/firewall.png?raw=true) | Concepts/firewall.puml
Concepts | OFF_FIREWALL_BLUE | ![firewall_blue](/office2014/Concepts/firewall_blue.png?raw=true) | Concepts/firewall_blue.puml
Concepts | OFF_FIREWALL_GHOSTED | ![firewall_ghosted](/office2014/Concepts/firewall_ghosted.png?raw=true) | Concepts/firewall_ghosted.puml
Concepts | OFF_FIREWALL_GREEN | ![firewall_green](/office2014/Concepts/firewall_green.png?raw=true) | Concepts/firewall_green.puml
Concepts | OFF_FIREWALL_ORANGE | ![firewall_orange](/office2014/Concepts/firewall_orange.png?raw=true) | Concepts/firewall_orange.puml
Concepts | OFF_FOLDER | ![folder](/office2014/Concepts/folder.png?raw=true) | Concepts/folder.puml
Concepts | OFF_FOLDERS | ![folders](/office2014/Concepts/folders.png?raw=true) | Concepts/folders.puml
Concepts | OFF_FOLDER_BLUE | ![folder_blue](/office2014/Concepts/folder_blue.png?raw=true) | Concepts/folder_blue.puml
Concepts | OFF_FOLDER_GHOSTED | ![folder_ghosted](/office2014/Concepts/folder_ghosted.png?raw=true) | Concepts/folder_ghosted.puml
Concepts | OFF_FOLDER_GREEN | ![folder_green](/office2014/Concepts/folder_green.png?raw=true) | Concepts/folder_green.puml
Concepts | OFF_FOLDER_OPEN | ![folder_open](/office2014/Concepts/folder_open.png?raw=true) | Concepts/folder_open.puml
Concepts | OFF_FOLDER_ORANGE | ![folder_orange](/office2014/Concepts/folder_orange.png?raw=true) | Concepts/folder_orange.puml
Concepts | OFF_FOLDER_PUBLIC | ![folder_public](/office2014/Concepts/folder_public.png?raw=true) | Concepts/folder_public.puml
Concepts | OFF_FOLDER_SHARED | ![folder_shared](/office2014/Concepts/folder_shared.png?raw=true) | Concepts/folder_shared.puml
Concepts | OFF_FORM | ![form](/office2014/Concepts/form.png?raw=true) | Concepts/form.puml
Concepts | OFF_GET_STARTED | ![get_started](/office2014/Concepts/get_started.png?raw=true) | Concepts/get_started.puml
Concepts | OFF_GLOBE_INTERNET | ![globe_internet](/office2014/Concepts/globe_internet.png?raw=true) | Concepts/globe_internet.puml
Concepts | OFF_HELP | ![help](/office2014/Concepts/help.png?raw=true) | Concepts/help.puml
Concepts | OFF_HOME | ![home](/office2014/Concepts/home.png?raw=true) | Concepts/home.puml
Concepts | OFF_HOME_BLUE | ![home_blue](/office2014/Concepts/home_blue.png?raw=true) | Concepts/home_blue.puml
Concepts | OFF_HOME_GHOSTED | ![home_ghosted](/office2014/Concepts/home_ghosted.png?raw=true) | Concepts/home_ghosted.puml
Concepts | OFF_HOME_GREEN | ![home_green](/office2014/Concepts/home_green.png?raw=true) | Concepts/home_green.puml
Concepts | OFF_HOME_ORANGE | ![home_orange](/office2014/Concepts/home_orange.png?raw=true) | Concepts/home_orange.puml
Concepts | OFF_HOME_PAGE | ![home_page](/office2014/Concepts/home_page.png?raw=true) | Concepts/home_page.puml
Concepts | OFF_HOME_PAGE_BLUE | ![home_page_blue](/office2014/Concepts/home_page_blue.png?raw=true) | Concepts/home_page_blue.puml
Concepts | OFF_HOME_PAGE_GHOSTED | ![home_page_ghosted](/office2014/Concepts/home_page_ghosted.png?raw=true) | Concepts/home_page_ghosted.puml
Concepts | OFF_HOME_PAGE_GREEN | ![home_page_green](/office2014/Concepts/home_page_green.png?raw=true) | Concepts/home_page_green.puml
Concepts | OFF_HOME_PAGE_ORANGE | ![home_page_orange](/office2014/Concepts/home_page_orange.png?raw=true) | Concepts/home_page_orange.puml
Concepts | OFF_HYBRID | ![hybrid](/office2014/Concepts/hybrid.png?raw=true) | Concepts/hybrid.puml
Concepts | OFF_INPUT_OUTPUT_FILTER | ![input_output_filter](/office2014/Concepts/input_output_filter.png?raw=true) | Concepts/input_output_filter.puml
Concepts | OFF_INSTALL | ![install](/office2014/Concepts/install.png?raw=true) | Concepts/install.puml
Concepts | OFF_INTEGRATION | ![integration](/office2014/Concepts/integration.png?raw=true) | Concepts/integration.puml
Concepts | OFF_LAB | ![lab](/office2014/Concepts/lab.png?raw=true) | Concepts/lab.puml
Concepts | OFF_LEARN | ![learn](/office2014/Concepts/learn.png?raw=true) | Concepts/learn.puml
Concepts | OFF_LICENSE | ![license](/office2014/Concepts/license.png?raw=true) | Concepts/license.puml
Concepts | OFF_LINK | ![link](/office2014/Concepts/link.png?raw=true) | Concepts/link.puml
Concepts | OFF_LIST_LIBRARY | ![list_library](/office2014/Concepts/list_library.png?raw=true) | Concepts/list_library.puml
Concepts | OFF_MAILBOX | ![mailbox](/office2014/Concepts/mailbox.png?raw=true) | Concepts/mailbox.puml
Concepts | OFF_MAILBOX2 | ![mailbox2](/office2014/Concepts/mailbox2.png?raw=true) | Concepts/mailbox2.puml
Concepts | OFF_MAINTENANCE | ![maintenance](/office2014/Concepts/maintenance.png?raw=true) | Concepts/maintenance.puml
Concepts | OFF_MARKETPLACE_SHOPPING_BAG | ![marketplace_shopping_bag](/office2014/Concepts/marketplace_shopping_bag.png?raw=true) | Concepts/marketplace_shopping_bag.puml
Concepts | OFF_MEETS_REQUIREMENTS | ![meets_requirements](/office2014/Concepts/meets_requirements.png?raw=true) | Concepts/meets_requirements.puml
Concepts | OFF_MIGRATION | ![migration](/office2014/Concepts/migration.png?raw=true) | Concepts/migration.puml
Concepts | OFF_MOES | ![moes](/office2014/Concepts/moes.png?raw=true) | Concepts/moes.puml
Concepts | OFF_NAVIGATION | ![navigation](/office2014/Concepts/navigation.png?raw=true) | Concepts/navigation.puml
Concepts | OFF_NODE_GENERIC | ![node_generic](/office2014/Concepts/node_generic.png?raw=true) | Concepts/node_generic.puml
Concepts | OFF_NODE_GENERIC_BLUE | ![node_generic_blue](/office2014/Concepts/node_generic_blue.png?raw=true) | Concepts/node_generic_blue.puml
Concepts | OFF_NODE_GENERIC_GHOSTED | ![node_generic_ghosted](/office2014/Concepts/node_generic_ghosted.png?raw=true) | Concepts/node_generic_ghosted.puml
Concepts | OFF_NODE_GENERIC_GREEN | ![node_generic_green](/office2014/Concepts/node_generic_green.png?raw=true) | Concepts/node_generic_green.puml
Concepts | OFF_NODE_GENERIC_ORANGE | ![node_generic_orange](/office2014/Concepts/node_generic_orange.png?raw=true) | Concepts/node_generic_orange.puml
Concepts | OFF_OFFICE_INSTALLED | ![office_installed](/office2014/Concepts/office_installed.png?raw=true) | Concepts/office_installed.puml
Concepts | OFF_ON_PREMISES | ![on_premises](/office2014/Concepts/on_premises.png?raw=true) | Concepts/on_premises.puml
Concepts | OFF_ON_PREMISES_DIRECTORY | ![on_premises_directory](/office2014/Concepts/on_premises_directory.png?raw=true) | Concepts/on_premises_directory.puml
Concepts | OFF_PHISHING | ![phishing](/office2014/Concepts/phishing.png?raw=true) | Concepts/phishing.puml
Concepts | OFF_PIN | ![pin](/office2014/Concepts/pin.png?raw=true) | Concepts/pin.puml
Concepts | OFF_PLATFORM_OPTIONS | ![platform_options](/office2014/Concepts/platform_options.png?raw=true) | Concepts/platform_options.puml
Concepts | OFF_PROPERTIES | ![properties](/office2014/Concepts/properties.png?raw=true) | Concepts/properties.puml
Concepts | OFF_PUBLISH | ![publish](/office2014/Concepts/publish.png?raw=true) | Concepts/publish.puml
Concepts | OFF_REMOTE_ACCESS | ![remote_access](/office2014/Concepts/remote_access.png?raw=true) | Concepts/remote_access.puml
Concepts | OFF_SCRIPT | ![script](/office2014/Concepts/script.png?raw=true) | Concepts/script.puml
Concepts | OFF_SEARCH | ![search](/office2014/Concepts/search.png?raw=true) | Concepts/search.puml
Concepts | OFF_SERVICE_APPLICATION | ![service_application](/office2014/Concepts/service_application.png?raw=true) | Concepts/service_application.puml
Concepts | OFF_SETTINGS | ![settings](/office2014/Concepts/settings.png?raw=true) | Concepts/settings.puml
Concepts | OFF_SETTINGS_OFFICE_365 | ![settings_office_365](/office2014/Concepts/settings_office_365.png?raw=true) | Concepts/settings_office_365.puml
Concepts | OFF_SIGN_UP | ![sign_up](/office2014/Concepts/sign_up.png?raw=true) | Concepts/sign_up.puml
Concepts | OFF_SOUND_FILE | ![sound_file](/office2014/Concepts/sound_file.png?raw=true) | Concepts/sound_file.puml
Concepts | OFF_TASKS | ![tasks](/office2014/Concepts/tasks.png?raw=true) | Concepts/tasks.puml
Concepts | OFF_TECHNICAL_DIAGRAM | ![technical_diagram](/office2014/Concepts/technical_diagram.png?raw=true) | Concepts/technical_diagram.puml
Concepts | OFF_UPGRADE_APPLICATION | ![upgrade_application](/office2014/Concepts/upgrade_application.png?raw=true) | Concepts/upgrade_application.puml
Concepts | OFF_UPGRADE_SERVER | ![upgrade_server](/office2014/Concepts/upgrade_server.png?raw=true) | Concepts/upgrade_server.puml
Concepts | OFF_UPGRADE_SITE | ![upgrade_site](/office2014/Concepts/upgrade_site.png?raw=true) | Concepts/upgrade_site.puml
Concepts | OFF_UPLOAD | ![upload](/office2014/Concepts/upload.png?raw=true) | Concepts/upload.puml
Concepts | OFF_VIDEO_PLAY | ![video_play](/office2014/Concepts/video_play.png?raw=true) | Concepts/video_play.puml
Concepts | OFF_VIEW_FORM | ![view_form](/office2014/Concepts/view_form.png?raw=true) | Concepts/view_form.puml
Concepts | OFF_VOICEMAIL | ![voicemail](/office2014/Concepts/voicemail.png?raw=true) | Concepts/voicemail.puml
Concepts | OFF_VOICEMAIL_PREVIEW | ![voicemail_preview](/office2014/Concepts/voicemail_preview.png?raw=true) | Concepts/voicemail_preview.puml
Concepts | OFF_WALKTHROUGH | ![walkthrough](/office2014/Concepts/walkthrough.png?raw=true) | Concepts/walkthrough.puml
Concepts | OFF_WEBSITE | ![website](/office2014/Concepts/website.png?raw=true) | Concepts/website.puml
Concepts | OFF_WEB_CONFERENCING | ![web_conferencing](/office2014/Concepts/web_conferencing.png?raw=true) | Concepts/web_conferencing.puml
Concepts | OFF_WEB_PAGE | ![web_page](/office2014/Concepts/web_page.png?raw=true) | Concepts/web_page.puml
Concepts | OFF_WEB_PART | ![web_part](/office2014/Concepts/web_part.png?raw=true) | Concepts/web_part.puml
Concepts | OFF_WEB_SERVICES | ![web_services](/office2014/Concepts/web_services.png?raw=true) | Concepts/web_services.puml
Concepts | OFF_WHATS_NEW | ![whats_new](/office2014/Concepts/whats_new.png?raw=true) | Concepts/whats_new.puml
Concepts | OFF_WINDOWS_POWERSHELL | ![windows_powershell](/office2014/Concepts/windows_powershell.png?raw=true) | Concepts/windows_powershell.puml
Concepts | OFF_WRITING_PEN | ![writing_pen](/office2014/Concepts/writing_pen.png?raw=true) | Concepts/writing_pen.puml
Concepts | OFF_WRITING_PENCIL | ![writing_pencil](/office2014/Concepts/writing_pencil.png?raw=true) | Concepts/writing_pencil.puml
Databases | OFF_ADDRESS_BOOK_STORE | ![address_book_store](/office2014/Databases/address_book_store.png?raw=true) | Databases/address_book_store.puml
Databases | OFF_APPLICATION_STORE | ![application_store](/office2014/Databases/application_store.png?raw=true) | Databases/application_store.puml
Databases | OFF_DATABASE | ![database](/office2014/Databases/database.png?raw=true) | Databases/database.puml
Databases | OFF_DATABASE_AVAILABILITY_GROUP | ![database_availability_group](/office2014/Databases/database_availability_group.png?raw=true) | Databases/database_availability_group.puml
Databases | OFF_DATABASE_BLUE | ![database_blue](/office2014/Databases/database_blue.png?raw=true) | Databases/database_blue.puml
Databases | OFF_DATABASE_CUBE | ![database_cube](/office2014/Databases/database_cube.png?raw=true) | Databases/database_cube.puml
Databases | OFF_DATABASE_CUBE_BLUE | ![database_cube_blue](/office2014/Databases/database_cube_blue.png?raw=true) | Databases/database_cube_blue.puml
Databases | OFF_DATABASE_CUBE_GHOSTED | ![database_cube_ghosted](/office2014/Databases/database_cube_ghosted.png?raw=true) | Databases/database_cube_ghosted.puml
Databases | OFF_DATABASE_CUBE_GREEN | ![database_cube_green](/office2014/Databases/database_cube_green.png?raw=true) | Databases/database_cube_green.puml
Databases | OFF_DATABASE_CUBE_ORANGE | ![database_cube_orange](/office2014/Databases/database_cube_orange.png?raw=true) | Databases/database_cube_orange.puml
Databases | OFF_DATABASE_GHOSTED | ![database_ghosted](/office2014/Databases/database_ghosted.png?raw=true) | Databases/database_ghosted.puml
Databases | OFF_DATABASE_GREEN | ![database_green](/office2014/Databases/database_green.png?raw=true) | Databases/database_green.puml
Databases | OFF_DATABASE_MINI_1 | ![database_mini_1](/office2014/Databases/database_mini_1.png?raw=true) | Databases/database_mini_1.puml
Databases | OFF_DATABASE_MINI_1_BLUE | ![database_mini_1_blue](/office2014/Databases/database_mini_1_blue.png?raw=true) | Databases/database_mini_1_blue.puml
Databases | OFF_DATABASE_MINI_1_GHOSTED | ![database_mini_1_ghosted](/office2014/Databases/database_mini_1_ghosted.png?raw=true) | Databases/database_mini_1_ghosted.puml
Databases | OFF_DATABASE_MINI_1_GREEN | ![database_mini_1_green](/office2014/Databases/database_mini_1_green.png?raw=true) | Databases/database_mini_1_green.puml
Databases | OFF_DATABASE_MINI_1_ORANGE | ![database_mini_1_orange](/office2014/Databases/database_mini_1_orange.png?raw=true) | Databases/database_mini_1_orange.puml
Databases | OFF_DATABASE_MINI_2 | ![database_mini_2](/office2014/Databases/database_mini_2.png?raw=true) | Databases/database_mini_2.puml
Databases | OFF_DATABASE_MINI_2_BLUE | ![database_mini_2_blue](/office2014/Databases/database_mini_2_blue.png?raw=true) | Databases/database_mini_2_blue.puml
Databases | OFF_DATABASE_MINI_2_GHOSTED | ![database_mini_2_ghosted](/office2014/Databases/database_mini_2_ghosted.png?raw=true) | Databases/database_mini_2_ghosted.puml
Databases | OFF_DATABASE_MINI_2_GREEN | ![database_mini_2_green](/office2014/Databases/database_mini_2_green.png?raw=true) | Databases/database_mini_2_green.puml
Databases | OFF_DATABASE_MINI_2_ORANGE | ![database_mini_2_orange](/office2014/Databases/database_mini_2_orange.png?raw=true) | Databases/database_mini_2_orange.puml
Databases | OFF_DATABASE_MINI_3 | ![database_mini_3](/office2014/Databases/database_mini_3.png?raw=true) | Databases/database_mini_3.puml
Databases | OFF_DATABASE_MINI_3_BLUE | ![database_mini_3_blue](/office2014/Databases/database_mini_3_blue.png?raw=true) | Databases/database_mini_3_blue.puml
Databases | OFF_DATABASE_MINI_3_GHOSTED | ![database_mini_3_ghosted](/office2014/Databases/database_mini_3_ghosted.png?raw=true) | Databases/database_mini_3_ghosted.puml
Databases | OFF_DATABASE_MINI_3_GREEN | ![database_mini_3_green](/office2014/Databases/database_mini_3_green.png?raw=true) | Databases/database_mini_3_green.puml
Databases | OFF_DATABASE_MINI_3_ORANGE | ![database_mini_3_orange](/office2014/Databases/database_mini_3_orange.png?raw=true) | Databases/database_mini_3_orange.puml
Databases | OFF_DATABASE_MIRROR | ![database_mirror](/office2014/Databases/database_mirror.png?raw=true) | Databases/database_mirror.puml
Databases | OFF_DATABASE_MIRROR_WITNESS_NODE | ![database_mirror_witness_node](/office2014/Databases/database_mirror_witness_node.png?raw=true) | Databases/database_mirror_witness_node.puml
Databases | OFF_DATABASE_ORANGE | ![database_orange](/office2014/Databases/database_orange.png?raw=true) | Databases/database_orange.puml
Databases | OFF_DATABASE_PARTITION_2 | ![database_partition_2](/office2014/Databases/database_partition_2.png?raw=true) | Databases/database_partition_2.puml
Databases | OFF_DATABASE_PARTITION_3 | ![database_partition_3](/office2014/Databases/database_partition_3.png?raw=true) | Databases/database_partition_3.puml
Databases | OFF_DATABASE_PARTITION_4 | ![database_partition_4](/office2014/Databases/database_partition_4.png?raw=true) | Databases/database_partition_4.puml
Databases | OFF_DATABASE_PARTITION_5 | ![database_partition_5](/office2014/Databases/database_partition_5.png?raw=true) | Databases/database_partition_5.puml
Databases | OFF_DATABASE_PUBLIC_FOLDER | ![database_public_folder](/office2014/Databases/database_public_folder.png?raw=true) | Databases/database_public_folder.puml
Databases | OFF_DATABASE_SERVER | ![database_server](/office2014/Databases/database_server.png?raw=true) | Databases/database_server.puml
Databases | OFF_DATABASE_SERVER_BLUE | ![database_server_blue](/office2014/Databases/database_server_blue.png?raw=true) | Databases/database_server_blue.puml
Databases | OFF_DATABASE_SERVER_GHOSTED | ![database_server_ghosted](/office2014/Databases/database_server_ghosted.png?raw=true) | Databases/database_server_ghosted.puml
Databases | OFF_DATABASE_SERVER_GREEN | ![database_server_green](/office2014/Databases/database_server_green.png?raw=true) | Databases/database_server_green.puml
Databases | OFF_DATABASE_SERVER_ORANGE | ![database_server_orange](/office2014/Databases/database_server_orange.png?raw=true) | Databases/database_server_orange.puml
Databases | OFF_MAILBOX_DATABASE | ![mailbox_database](/office2014/Databases/mailbox_database.png?raw=true) | Databases/mailbox_database.puml
Databases | OFF_MONITORING_STORE | ![monitoring_store](/office2014/Databases/monitoring_store.png?raw=true) | Databases/monitoring_store.puml
Databases | OFF_UNIFIED_CONTACT_STORE | ![unified_contact_store](/office2014/Databases/unified_contact_store.png?raw=true) | Databases/unified_contact_store.puml
Databases | OFF_WEB_STORE | ![web_store](/office2014/Databases/web_store.png?raw=true) | Databases/web_store.puml
Devices | OFF_CD_DVD | ![cd_dvd](/office2014/Devices/cd_dvd.png?raw=true) | Devices/cd_dvd.puml
Devices | OFF_CELL_PHONE_ANDROID_PROPORTIONAL | ![cell_phone_android_proportional](/office2014/Devices/cell_phone_android_proportional.png?raw=true) | Devices/cell_phone_android_proportional.puml
Devices | OFF_CELL_PHONE_ANDROID_STAND_ALONE | ![cell_phone_android_stand_alone](/office2014/Devices/cell_phone_android_stand_alone.png?raw=true) | Devices/cell_phone_android_stand_alone.puml
Devices | OFF_CELL_PHONE_GENERIC | ![cell_phone_generic](/office2014/Devices/cell_phone_generic.png?raw=true) | Devices/cell_phone_generic.puml
Devices | OFF_CELL_PHONE_IPHONE_PROPORTIONAL | ![cell_phone_iphone_proportional](/office2014/Devices/cell_phone_iphone_proportional.png?raw=true) | Devices/cell_phone_iphone_proportional.puml
Devices | OFF_CELL_PHONE_IPHONE_STAND_ALONE | ![cell_phone_iphone_stand_alone](/office2014/Devices/cell_phone_iphone_stand_alone.png?raw=true) | Devices/cell_phone_iphone_stand_alone.puml
Devices | OFF_CELL_PHONE_WINDOWS_PHONE_PROPORTIONAL | ![cell_phone_windows_phone_proportional](/office2014/Devices/cell_phone_windows_phone_proportional.png?raw=true) | Devices/cell_phone_windows_phone_proportional.puml
Devices | OFF_CELL_PHONE_WINDOWS_PHONE_STAND_ALONE | ![cell_phone_windows_phone_stand_alone](/office2014/Devices/cell_phone_windows_phone_stand_alone.png?raw=true) | Devices/cell_phone_windows_phone_stand_alone.puml
Devices | OFF_DATA_JACK | ![data_jack](/office2014/Devices/data_jack.png?raw=true) | Devices/data_jack.puml
Devices | OFF_DEVICE_BLUETOOTH | ![device_bluetooth](/office2014/Devices/device_bluetooth.png?raw=true) | Devices/device_bluetooth.puml
Devices | OFF_DEVICE_FAX | ![device_fax](/office2014/Devices/device_fax.png?raw=true) | Devices/device_fax.puml
Devices | OFF_DEVICE_HEADSET | ![device_headset](/office2014/Devices/device_headset.png?raw=true) | Devices/device_headset.puml
Devices | OFF_DEVICE_LAPTOP | ![device_laptop](/office2014/Devices/device_laptop.png?raw=true) | Devices/device_laptop.puml
Devices | OFF_DEVICE_LCD_MONITOR | ![device_lcd_monitor](/office2014/Devices/device_lcd_monitor.png?raw=true) | Devices/device_lcd_monitor.puml
Devices | OFF_DEVICE_MAC_CLIENT | ![device_mac_client](/office2014/Devices/device_mac_client.png?raw=true) | Devices/device_mac_client.puml
Devices | OFF_DEVICE_MICROPHONE | ![device_microphone](/office2014/Devices/device_microphone.png?raw=true) | Devices/device_microphone.puml
Devices | OFF_DEVICE_PHONE_DIGITAL | ![device_phone_digital](/office2014/Devices/device_phone_digital.png?raw=true) | Devices/device_phone_digital.puml
Devices | OFF_DEVICE_PHONE_TRADITIONAL | ![device_phone_traditional](/office2014/Devices/device_phone_traditional.png?raw=true) | Devices/device_phone_traditional.puml
Devices | OFF_DEVICE_PHONE_USB | ![device_phone_usb](/office2014/Devices/device_phone_usb.png?raw=true) | Devices/device_phone_usb.puml
Devices | OFF_DEVICE_PHONE_VOIP | ![device_phone_voip](/office2014/Devices/device_phone_voip.png?raw=true) | Devices/device_phone_voip.puml
Devices | OFF_DEVICE_PRINTER | ![device_printer](/office2014/Devices/device_printer.png?raw=true) | Devices/device_printer.puml
Devices | OFF_DEVICE_ROUNDTABLE | ![device_roundtable](/office2014/Devices/device_roundtable.png?raw=true) | Devices/device_roundtable.puml
Devices | OFF_DEVICE_STYLUS | ![device_stylus](/office2014/Devices/device_stylus.png?raw=true) | Devices/device_stylus.puml
Devices | OFF_DEVICE_TABLET_ANDROID | ![device_tablet_android](/office2014/Devices/device_tablet_android.png?raw=true) | Devices/device_tablet_android.puml
Devices | OFF_DEVICE_TABLET_IPAD | ![device_tablet_ipad](/office2014/Devices/device_tablet_ipad.png?raw=true) | Devices/device_tablet_ipad.puml
Devices | OFF_DEVICE_TABLET_IPAD_MINI | ![device_tablet_ipad_mini](/office2014/Devices/device_tablet_ipad_mini.png?raw=true) | Devices/device_tablet_ipad_mini.puml
Devices | OFF_DEVICE_TABLET_WINDOWS_7_INCH | ![device_tablet_windows_7_inch](/office2014/Devices/device_tablet_windows_7_inch.png?raw=true) | Devices/device_tablet_windows_7_inch.puml
Devices | OFF_DEVICE_TABLET_WINDOWS_8 | ![device_tablet_windows_8](/office2014/Devices/device_tablet_windows_8.png?raw=true) | Devices/device_tablet_windows_8.puml
Devices | OFF_DEVICE_TV | ![device_tv](/office2014/Devices/device_tv.png?raw=true) | Devices/device_tv.puml
Devices | OFF_DEVICE_UPDATE_SERVICE | ![device_update_service](/office2014/Devices/device_update_service.png?raw=true) | Devices/device_update_service.puml
Devices | OFF_DEVICE_WEBCAM | ![device_webcam](/office2014/Devices/device_webcam.png?raw=true) | Devices/device_webcam.puml
Devices | OFF_DEVICE_WEBCAM_HD | ![device_webcam_hd](/office2014/Devices/device_webcam_hd.png?raw=true) | Devices/device_webcam_hd.puml
Devices | OFF_HARD_DISK | ![hard_disk](/office2014/Devices/hard_disk.png?raw=true) | Devices/hard_disk.puml
Devices | OFF_IP_GATEWAY | ![ip_gateway](/office2014/Devices/ip_gateway.png?raw=true) | Devices/ip_gateway.puml
Devices | OFF_IP_PBX | ![ip_pbx](/office2014/Devices/ip_pbx.png?raw=true) | Devices/ip_pbx.puml
Devices | OFF_LOAD_BALANCER | ![load_balancer](/office2014/Devices/load_balancer.png?raw=true) | Devices/load_balancer.puml
Devices | OFF_MANAGEMENT_CONSOLE | ![management_console](/office2014/Devices/management_console.png?raw=true) | Devices/management_console.puml
Devices | OFF_MODEM | ![modem](/office2014/Devices/modem.png?raw=true) | Devices/modem.puml
Devices | OFF_NIC | ![nic](/office2014/Devices/nic.png?raw=true) | Devices/nic.puml
Devices | OFF_ROUTER | ![router](/office2014/Devices/router.png?raw=true) | Devices/router.puml
Devices | OFF_SESSION_BORDER_CONTROLLER | ![session_border_controller](/office2014/Devices/session_border_controller.png?raw=true) | Devices/session_border_controller.puml
Devices | OFF_SHADOWED_ROUTER | ![shadowed_router](/office2014/Devices/shadowed_router.png?raw=true) | Devices/shadowed_router.puml
Devices | OFF_SWITCH | ![switch](/office2014/Devices/switch.png?raw=true) | Devices/switch.puml
Devices | OFF_VIDEO_CAMERA | ![video_camera](/office2014/Devices/video_camera.png?raw=true) | Devices/video_camera.puml
Devices | OFF_VIDEO_GATEWAY | ![video_gateway](/office2014/Devices/video_gateway.png?raw=true) | Devices/video_gateway.puml
Devices | OFF_WORKSTATION | ![workstation](/office2014/Devices/workstation.png?raw=true) | Devices/workstation.puml
Devices | OFF_WORKSTATION_PC | ![workstation_pc](/office2014/Devices/workstation_pc.png?raw=true) | Devices/workstation_pc.puml
Devices | OFF_WORKSTATION_VISUAL_STUDIO | ![workstation_visual_studio](/office2014/Devices/workstation_visual_studio.png?raw=true) | Devices/workstation_visual_studio.puml
Security | OFF_ACTIVE_DIRECTORY | ![active_directory](/office2014/Security/active_directory.png?raw=true) | Security/active_directory.puml
Security | OFF_ADDRESS_BOOK_POLICIES | ![address_book_policies](/office2014/Security/address_book_policies.png?raw=true) | Security/address_book_policies.puml
Security | OFF_CERTIFICATE | ![certificate](/office2014/Security/certificate.png?raw=true) | Security/certificate.puml
Security | OFF_CREDENTIALS | ![credentials](/office2014/Security/credentials.png?raw=true) | Security/credentials.puml
Security | OFF_DOMAIN | ![domain](/office2014/Security/domain.png?raw=true) | Security/domain.puml
Security | OFF_EMAIL_ADDRESS_POLICY | ![email_address_policy](/office2014/Security/email_address_policy.png?raw=true) | Security/email_address_policy.puml
Security | OFF_FEDERATION_SERVICE | ![federation_service](/office2014/Security/federation_service.png?raw=true) | Security/federation_service.puml
Security | OFF_FEDERATION_TRUST | ![federation_trust](/office2014/Security/federation_trust.png?raw=true) | Security/federation_trust.puml
Security | OFF_IRM_PROTECTED_MESSAGE | ![irm_protected_message](/office2014/Security/irm_protected_message.png?raw=true) | Security/irm_protected_message.puml
Security | OFF_KEY_PERMISSIONS | ![key_permissions](/office2014/Security/key_permissions.png?raw=true) | Security/key_permissions.puml
Security | OFF_KEY_PERMISSIONS_BLUE | ![key_permissions_blue](/office2014/Security/key_permissions_blue.png?raw=true) | Security/key_permissions_blue.puml
Security | OFF_KEY_PERMISSIONS_GHOSTED | ![key_permissions_ghosted](/office2014/Security/key_permissions_ghosted.png?raw=true) | Security/key_permissions_ghosted.puml
Security | OFF_KEY_PERMISSIONS_GREEN | ![key_permissions_green](/office2014/Security/key_permissions_green.png?raw=true) | Security/key_permissions_green.puml
Security | OFF_KEY_PERMISSIONS_ORANGE | ![key_permissions_orange](/office2014/Security/key_permissions_orange.png?raw=true) | Security/key_permissions_orange.puml
Security | OFF_LOCK_PROTECTED | ![lock_protected](/office2014/Security/lock_protected.png?raw=true) | Security/lock_protected.puml
Security | OFF_LOCK_PROTECTED_BLUE | ![lock_protected_blue](/office2014/Security/lock_protected_blue.png?raw=true) | Security/lock_protected_blue.puml
Security | OFF_LOCK_PROTECTED_GHOSTED | ![lock_protected_ghosted](/office2014/Security/lock_protected_ghosted.png?raw=true) | Security/lock_protected_ghosted.puml
Security | OFF_LOCK_PROTECTED_GREEN | ![lock_protected_green](/office2014/Security/lock_protected_green.png?raw=true) | Security/lock_protected_green.puml
Security | OFF_LOCK_PROTECTED_ORANGE | ![lock_protected_orange](/office2014/Security/lock_protected_orange.png?raw=true) | Security/lock_protected_orange.puml
Security | OFF_LOCK_UNPROTECTED | ![lock_unprotected](/office2014/Security/lock_unprotected.png?raw=true) | Security/lock_unprotected.puml
Security | OFF_LOCK_UNPROTECTED_BLUE | ![lock_unprotected_blue](/office2014/Security/lock_unprotected_blue.png?raw=true) | Security/lock_unprotected_blue.puml
Security | OFF_LOCK_UNPROTECTED_GHOSTED | ![lock_unprotected_ghosted](/office2014/Security/lock_unprotected_ghosted.png?raw=true) | Security/lock_unprotected_ghosted.puml
Security | OFF_LOCK_UNPROTECTED_GREEN | ![lock_unprotected_green](/office2014/Security/lock_unprotected_green.png?raw=true) | Security/lock_unprotected_green.puml
Security | OFF_LOCK_UNPROTECTED_ORANGE | ![lock_unprotected_orange](/office2014/Security/lock_unprotected_orange.png?raw=true) | Security/lock_unprotected_orange.puml
Security | OFF_LOCK_WITH_KEY_SECURITY | ![lock_with_key_security](/office2014/Security/lock_with_key_security.png?raw=true) | Security/lock_with_key_security.puml
Security | OFF_LOCK_WITH_KEY_SECURITY_BLUE | ![lock_with_key_security_blue](/office2014/Security/lock_with_key_security_blue.png?raw=true) | Security/lock_with_key_security_blue.puml
Security | OFF_LOCK_WITH_KEY_SECURITY_GHOSTED | ![lock_with_key_security_ghosted](/office2014/Security/lock_with_key_security_ghosted.png?raw=true) | Security/lock_with_key_security_ghosted.puml
Security | OFF_LOCK_WITH_KEY_SECURITY_GREEN | ![lock_with_key_security_green](/office2014/Security/lock_with_key_security_green.png?raw=true) | Security/lock_with_key_security_green.puml
Security | OFF_LOCK_WITH_KEY_SECURITY_ORANGE | ![lock_with_key_security_orange](/office2014/Security/lock_with_key_security_orange.png?raw=true) | Security/lock_with_key_security_orange.puml
Security | OFF_MANAGEMENT_ROLE | ![management_role](/office2014/Security/management_role.png?raw=true) | Security/management_role.puml
Security | OFF_POLICY | ![policy](/office2014/Security/policy.png?raw=true) | Security/policy.puml
Security | OFF_PROTECTED_VOICE_MAIL | ![protected_voice_mail](/office2014/Security/protected_voice_mail.png?raw=true) | Security/protected_voice_mail.puml
Security | OFF_RETENTION_POLICY | ![retention_policy](/office2014/Security/retention_policy.png?raw=true) | Security/retention_policy.puml
Security | OFF_RETENTION_POLICY_TAG | ![retention_policy_tag](/office2014/Security/retention_policy_tag.png?raw=true) | Security/retention_policy_tag.puml
Security | OFF_ROLE_ASSIGNMENT_POLICY | ![role_assignment_policy](/office2014/Security/role_assignment_policy.png?raw=true) | Security/role_assignment_policy.puml
Security | OFF_ROLE_GROUP | ![role_group](/office2014/Security/role_group.png?raw=true) | Security/role_group.puml
Security | OFF_SECURE_MESSAGING | ![secure_messaging](/office2014/Security/secure_messaging.png?raw=true) | Security/secure_messaging.puml
Security | OFF_SECURITY_ACCESS_PORTAL | ![security_access_portal](/office2014/Security/security_access_portal.png?raw=true) | Security/security_access_portal.puml
Security | OFF_SHARING_POLICY | ![sharing_policy](/office2014/Security/sharing_policy.png?raw=true) | Security/sharing_policy.puml
Security | OFF_SPLIT_DOMAIN_USER | ![split_domain_user](/office2014/Security/split_domain_user.png?raw=true) | Security/split_domain_user.puml
Security | OFF_TOKEN | ![token](/office2014/Security/token.png?raw=true) | Security/token.puml
Security | OFF_TOKEN_SERVICE | ![token_service](/office2014/Security/token_service.png?raw=true) | Security/token_service.puml
Security | OFF_TRUSTED_APPLICATION_SERVER | ![trusted_application_server](/office2014/Security/trusted_application_server.png?raw=true) | Security/trusted_application_server.puml
Security | OFF_UM_MAILBOX_POLICY | ![um_mailbox_policy](/office2014/Security/um_mailbox_policy.png?raw=true) | Security/um_mailbox_policy.puml
Security | OFF_UNIVERSAL_SECURITY_GROUP | ![universal_security_group](/office2014/Security/universal_security_group.png?raw=true) | Security/universal_security_group.puml
Servers | OFF_3RD_PARTY_MAIL_SERVER | ![3rd_party_mail_server](/office2014/Servers/3rd_party_mail_server.png?raw=true) | Servers/3rd_party_mail_server.puml
Servers | OFF_ACTIVE_DIRECTORY_FEDERATION_SERVICES_PROXY | ![active_directory_federation_services_proxy](/office2014/Servers/active_directory_federation_services_proxy.png?raw=true) | Servers/active_directory_federation_services_proxy.puml
Servers | OFF_ACTIVE_DIRECTORY_FEDERATION_SERVICES_SERVER | ![active_directory_federation_services_server](/office2014/Servers/active_directory_federation_services_server.png?raw=true) | Servers/active_directory_federation_services_server.puml
Servers | OFF_ACTIVE_DIRECTORY_FEDERATION_SERVICES_SERVER_BLUE | ![active_directory_federation_services_server_blue](/office2014/Servers/active_directory_federation_services_server_blue.png?raw=true) | Servers/active_directory_federation_services_server_blue.puml
Servers | OFF_ACTIVE_DIRECTORY_FEDERATION_SERVICES_SERVER_GHOSTED | ![active_directory_federation_services_server_ghosted](/office2014/Servers/active_directory_federation_services_server_ghosted.png?raw=true) | Servers/active_directory_federation_services_server_ghosted.puml
Servers | OFF_ACTIVE_DIRECTORY_FEDERATION_SERVICES_SERVER_GREEN | ![active_directory_federation_services_server_green](/office2014/Servers/active_directory_federation_services_server_green.png?raw=true) | Servers/active_directory_federation_services_server_green.puml
Servers | OFF_ACTIVE_DIRECTORY_FEDERATION_SERVICES_SERVER_ORANGE | ![active_directory_federation_services_server_orange](/office2014/Servers/active_directory_federation_services_server_orange.png?raw=true) | Servers/active_directory_federation_services_server_orange.puml
Servers | OFF_APPLICATION_SERVER | ![application_server](/office2014/Servers/application_server.png?raw=true) | Servers/application_server.puml
Servers | OFF_APPLICATION_SERVER_BLUE | ![application_server_blue](/office2014/Servers/application_server_blue.png?raw=true) | Servers/application_server_blue.puml
Servers | OFF_APPLICATION_SERVER_GHOSTED | ![application_server_ghosted](/office2014/Servers/application_server_ghosted.png?raw=true) | Servers/application_server_ghosted.puml
Servers | OFF_APPLICATION_SERVER_GREEN | ![application_server_green](/office2014/Servers/application_server_green.png?raw=true) | Servers/application_server_green.puml
Servers | OFF_APPLICATION_SERVER_ORANGE | ![application_server_orange](/office2014/Servers/application_server_orange.png?raw=true) | Servers/application_server_orange.puml
Servers | OFF_CALL_ADMISSION_CONTROL_SERVICE | ![call_admission_control_service](/office2014/Servers/call_admission_control_service.png?raw=true) | Servers/call_admission_control_service.puml
Servers | OFF_CERTIFICATE_AUTHORITY | ![certificate_authority](/office2014/Servers/certificate_authority.png?raw=true) | Servers/certificate_authority.puml
Servers | OFF_CLUSTER_SERVER | ![cluster_server](/office2014/Servers/cluster_server.png?raw=true) | Servers/cluster_server.puml
Servers | OFF_CLUSTER_SERVER_BLUE | ![cluster_server_blue](/office2014/Servers/cluster_server_blue.png?raw=true) | Servers/cluster_server_blue.puml
Servers | OFF_CLUSTER_SERVER_GHOSTED | ![cluster_server_ghosted](/office2014/Servers/cluster_server_ghosted.png?raw=true) | Servers/cluster_server_ghosted.puml
Servers | OFF_CLUSTER_SERVER_GREEN | ![cluster_server_green](/office2014/Servers/cluster_server_green.png?raw=true) | Servers/cluster_server_green.puml
Servers | OFF_CLUSTER_SERVER_ORANGE | ![cluster_server_orange](/office2014/Servers/cluster_server_orange.png?raw=true) | Servers/cluster_server_orange.puml
Servers | OFF_DATABASE_SERVER | ![database_server](/office2014/Servers/database_server.png?raw=true) | Servers/database_server.puml
Servers | OFF_DATABASE_SERVER_BLUE | ![database_server_blue](/office2014/Servers/database_server_blue.png?raw=true) | Servers/database_server_blue.puml
Servers | OFF_DATABASE_SERVER_GHOSTED | ![database_server_ghosted](/office2014/Servers/database_server_ghosted.png?raw=true) | Servers/database_server_ghosted.puml
Servers | OFF_DATABASE_SERVER_GREEN | ![database_server_green](/office2014/Servers/database_server_green.png?raw=true) | Servers/database_server_green.puml
Servers | OFF_DATABASE_SERVER_ORANGE | ![database_server_orange](/office2014/Servers/database_server_orange.png?raw=true) | Servers/database_server_orange.puml
Servers | OFF_DATACENTER | ![datacenter](/office2014/Servers/datacenter.png?raw=true) | Servers/datacenter.puml
Servers | OFF_DIRSYNC_SERVER | ![dirsync_server](/office2014/Servers/dirsync_server.png?raw=true) | Servers/dirsync_server.puml
Servers | OFF_DOMAIN_CONTROLLER | ![domain_controller](/office2014/Servers/domain_controller.png?raw=true) | Servers/domain_controller.puml
Servers | OFF_EXCHANGE_2010_CLIENT_ACCESS_SERVER_ROLE | ![exchange_2010_client_access_server_role](/office2014/Servers/exchange_2010_client_access_server_role.png?raw=true) | Servers/exchange_2010_client_access_server_role.puml
Servers | OFF_EXCHANGE_2010_EDGE_TRANSPORT_SERVER_ROLE | ![exchange_2010_edge_transport_server_role](/office2014/Servers/exchange_2010_edge_transport_server_role.png?raw=true) | Servers/exchange_2010_edge_transport_server_role.puml
Servers | OFF_EXCHANGE_2010_HUB_TRANSPORT_SERVER_ROLE | ![exchange_2010_hub_transport_server_role](/office2014/Servers/exchange_2010_hub_transport_server_role.png?raw=true) | Servers/exchange_2010_hub_transport_server_role.puml
Servers | OFF_EXCHANGE_2010_MAILBOX_SERVER_ROLE | ![exchange_2010_mailbox_server_role](/office2014/Servers/exchange_2010_mailbox_server_role.png?raw=true) | Servers/exchange_2010_mailbox_server_role.puml
Servers | OFF_EXCHANGE_2010_UM_SERVER_ROLE | ![exchange_2010_um_server_role](/office2014/Servers/exchange_2010_um_server_role.png?raw=true) | Servers/exchange_2010_um_server_role.puml
Servers | OFF_EXCHANGE_2013_CLIENT_ACCESS_SERVER | ![exchange_2013_client_access_server](/office2014/Servers/exchange_2013_client_access_server.png?raw=true) | Servers/exchange_2013_client_access_server.puml
Servers | OFF_EXCHANGE_2013_EDGE_TRANSPORT_SERVER | ![exchange_2013_edge_transport_server](/office2014/Servers/exchange_2013_edge_transport_server.png?raw=true) | Servers/exchange_2013_edge_transport_server.puml
Servers | OFF_EXCHANGE_2013_MAILBOX_SERVER | ![exchange_2013_mailbox_server](/office2014/Servers/exchange_2013_mailbox_server.png?raw=true) | Servers/exchange_2013_mailbox_server.puml
Servers | OFF_EXCHANGE_2013_SERVER | ![exchange_2013_server](/office2014/Servers/exchange_2013_server.png?raw=true) | Servers/exchange_2013_server.puml
Servers | OFF_FILE_SERVER | ![file_server](/office2014/Servers/file_server.png?raw=true) | Servers/file_server.puml
Servers | OFF_HYBRID_SERVER | ![hybrid_server](/office2014/Servers/hybrid_server.png?raw=true) | Servers/hybrid_server.puml
Servers | OFF_MAINFRAME | ![mainframe](/office2014/Servers/mainframe.png?raw=true) | Servers/mainframe.puml
Servers | OFF_MAINFRAME_HOST | ![mainframe_host](/office2014/Servers/mainframe_host.png?raw=true) | Servers/mainframe_host.puml
Servers | OFF_MONITORING_SQL_REPORTING_SERVICES | ![monitoring_sql_reporting_services](/office2014/Servers/monitoring_sql_reporting_services.png?raw=true) | Servers/monitoring_sql_reporting_services.puml
Servers | OFF_NETWORK | ![network](/office2014/Servers/network.png?raw=true) | Servers/network.puml
Servers | OFF_OFFICE_WEB_APPS_SERVER | ![office_web_apps_server](/office2014/Servers/office_web_apps_server.png?raw=true) | Servers/office_web_apps_server.puml
Servers | OFF_ON_PREMISES_SERVER | ![on_premises_server](/office2014/Servers/on_premises_server.png?raw=true) | Servers/on_premises_server.puml
Servers | OFF_PHYSICAL_HOST_FARM_SOLID_BLUE | ![physical_host_farm_solid_blue](/office2014/Servers/physical_host_farm_solid_blue.png?raw=true) | Servers/physical_host_farm_solid_blue.puml
Servers | OFF_PHYSICAL_HOST_SOLID_BLUE | ![physical_host_solid_blue](/office2014/Servers/physical_host_solid_blue.png?raw=true) | Servers/physical_host_solid_blue.puml
Servers | OFF_REVERSE_PROXY | ![reverse_proxy](/office2014/Servers/reverse_proxy.png?raw=true) | Servers/reverse_proxy.puml
Servers | OFF_SCOM | ![scom](/office2014/Servers/scom.png?raw=true) | Servers/scom.puml
Servers | OFF_SERVER_DISASTER | ![server_disaster](/office2014/Servers/server_disaster.png?raw=true) | Servers/server_disaster.puml
Servers | OFF_SERVER_FARM | ![server_farm](/office2014/Servers/server_farm.png?raw=true) | Servers/server_farm.puml
Servers | OFF_SERVER_FARM_BLUE | ![server_farm_blue](/office2014/Servers/server_farm_blue.png?raw=true) | Servers/server_farm_blue.puml
Servers | OFF_SERVER_FARM_GHOSTED | ![server_farm_ghosted](/office2014/Servers/server_farm_ghosted.png?raw=true) | Servers/server_farm_ghosted.puml
Servers | OFF_SERVER_FARM_GREEN | ![server_farm_green](/office2014/Servers/server_farm_green.png?raw=true) | Servers/server_farm_green.puml
Servers | OFF_SERVER_FARM_ORANGE | ![server_farm_orange](/office2014/Servers/server_farm_orange.png?raw=true) | Servers/server_farm_orange.puml
Servers | OFF_SERVER_GENERIC | ![server_generic](/office2014/Servers/server_generic.png?raw=true) | Servers/server_generic.puml
Servers | OFF_SERVER_GENERIC_BLUE | ![server_generic_blue](/office2014/Servers/server_generic_blue.png?raw=true) | Servers/server_generic_blue.puml
Servers | OFF_SERVER_GENERIC_GHOSTED | ![server_generic_ghosted](/office2014/Servers/server_generic_ghosted.png?raw=true) | Servers/server_generic_ghosted.puml
Servers | OFF_SERVER_GENERIC_GREEN | ![server_generic_green](/office2014/Servers/server_generic_green.png?raw=true) | Servers/server_generic_green.puml
Servers | OFF_SERVER_GENERIC_ORANGE | ![server_generic_orange](/office2014/Servers/server_generic_orange.png?raw=true) | Servers/server_generic_orange.puml
Servers | OFF_SERVER_SIDE_CODE | ![server_side_code](/office2014/Servers/server_side_code.png?raw=true) | Servers/server_side_code.puml
Servers | OFF_SHAREPOINT_SERVER | ![sharepoint_server](/office2014/Servers/sharepoint_server.png?raw=true) | Servers/sharepoint_server.puml
Servers | OFF_SKYPE_FOR_BUSINESS_BACK_END_SERVER | ![skype_for_business_back_end_server](/office2014/Servers/skype_for_business_back_end_server.png?raw=true) | Servers/skype_for_business_back_end_server.puml
Servers | OFF_SKYPE_FOR_BUSINESS_BACK_END_SERVER_MIRROR | ![skype_for_business_back_end_server_mirror](/office2014/Servers/skype_for_business_back_end_server_mirror.png?raw=true) | Servers/skype_for_business_back_end_server_mirror.puml
Servers | OFF_SKYPE_FOR_BUSINESS_DIRECTOR | ![skype_for_business_director](/office2014/Servers/skype_for_business_director.png?raw=true) | Servers/skype_for_business_director.puml
Servers | OFF_SKYPE_FOR_BUSINESS_DIRECTOR_ARRAY | ![skype_for_business_director_array](/office2014/Servers/skype_for_business_director_array.png?raw=true) | Servers/skype_for_business_director_array.puml
Servers | OFF_SKYPE_FOR_BUSINESS_EDGE_SERVER | ![skype_for_business_edge_server](/office2014/Servers/skype_for_business_edge_server.png?raw=true) | Servers/skype_for_business_edge_server.puml
Servers | OFF_SKYPE_FOR_BUSINESS_EDGE_SERVER_POOL | ![skype_for_business_edge_server_pool](/office2014/Servers/skype_for_business_edge_server_pool.png?raw=true) | Servers/skype_for_business_edge_server_pool.puml
Servers | OFF_SKYPE_FOR_BUSINESS_FRONT_END_POOL | ![skype_for_business_front_end_pool](/office2014/Servers/skype_for_business_front_end_pool.png?raw=true) | Servers/skype_for_business_front_end_pool.puml
Servers | OFF_SKYPE_FOR_BUSINESS_FRONT_END_SERVER | ![skype_for_business_front_end_server](/office2014/Servers/skype_for_business_front_end_server.png?raw=true) | Servers/skype_for_business_front_end_server.puml
Servers | OFF_SKYPE_FOR_BUSINESS_MEDIATION_SERVER | ![skype_for_business_mediation_server](/office2014/Servers/skype_for_business_mediation_server.png?raw=true) | Servers/skype_for_business_mediation_server.puml
Servers | OFF_SKYPE_FOR_BUSINESS_MONITORING_SERVER | ![skype_for_business_monitoring_server](/office2014/Servers/skype_for_business_monitoring_server.png?raw=true) | Servers/skype_for_business_monitoring_server.puml
Servers | OFF_SKYPE_FOR_BUSINESS_PERSISTENT_CHAT_SERVER | ![skype_for_business_persistent_chat_server](/office2014/Servers/skype_for_business_persistent_chat_server.png?raw=true) | Servers/skype_for_business_persistent_chat_server.puml
Servers | OFF_SKYPE_FOR_BUSINESS_SERVER | ![skype_for_business_server](/office2014/Servers/skype_for_business_server.png?raw=true) | Servers/skype_for_business_server.puml
Servers | OFF_SQL_SERVER | ![sql_server](/office2014/Servers/sql_server.png?raw=true) | Servers/sql_server.puml
Servers | OFF_SURVIVABLE_BRANCH_APPLIANCE | ![survivable_branch_appliance](/office2014/Servers/survivable_branch_appliance.png?raw=true) | Servers/survivable_branch_appliance.puml
Servers | OFF_SURVIVABLE_BRANCH_SERVER | ![survivable_branch_server](/office2014/Servers/survivable_branch_server.png?raw=true) | Servers/survivable_branch_server.puml
Servers | OFF_TOPOLOGY_BUILDER | ![topology_builder](/office2014/Servers/topology_builder.png?raw=true) | Servers/topology_builder.puml
Servers | OFF_TRUSTED_APPLICATION_POOL | ![trusted_application_pool](/office2014/Servers/trusted_application_pool.png?raw=true) | Servers/trusted_application_pool.puml
Servers | OFF_TRUSTED_APPLICATION_SERVER | ![trusted_application_server](/office2014/Servers/trusted_application_server.png?raw=true) | Servers/trusted_application_server.puml
Servers | OFF_TUNNEL_ANGLED | ![tunnel_angled](/office2014/Servers/tunnel_angled.png?raw=true) | Servers/tunnel_angled.puml
Servers | OFF_TUNNEL_STRAIGHT | ![tunnel_straight](/office2014/Servers/tunnel_straight.png?raw=true) | Servers/tunnel_straight.puml
Servers | OFF_VIDEO_INTEROP_SERVER | ![video_interop_server](/office2014/Servers/video_interop_server.png?raw=true) | Servers/video_interop_server.puml
Servers | OFF_VIRTUAL_APPLICATION_SERVER | ![virtual_application_server](/office2014/Servers/virtual_application_server.png?raw=true) | Servers/virtual_application_server.puml
Servers | OFF_VIRTUAL_APPLICATION_SERVER_BLUE | ![virtual_application_server_blue](/office2014/Servers/virtual_application_server_blue.png?raw=true) | Servers/virtual_application_server_blue.puml
Servers | OFF_VIRTUAL_DATABASE_SERVER | ![virtual_database_server](/office2014/Servers/virtual_database_server.png?raw=true) | Servers/virtual_database_server.puml
Servers | OFF_VIRTUAL_DATABASE_SERVER_BLUE | ![virtual_database_server_blue](/office2014/Servers/virtual_database_server_blue.png?raw=true) | Servers/virtual_database_server_blue.puml
Servers | OFF_VIRTUAL_SERVER | ![virtual_server](/office2014/Servers/virtual_server.png?raw=true) | Servers/virtual_server.puml
Servers | OFF_VIRTUAL_SERVER_BLUE | ![virtual_server_blue](/office2014/Servers/virtual_server_blue.png?raw=true) | Servers/virtual_server_blue.puml
Servers | OFF_VIRTUAL_WEB_SERVER | ![virtual_web_server](/office2014/Servers/virtual_web_server.png?raw=true) | Servers/virtual_web_server.puml
Servers | OFF_VIRTUAL_WEB_SERVER_BLUE | ![virtual_web_server_blue](/office2014/Servers/virtual_web_server_blue.png?raw=true) | Servers/virtual_web_server_blue.puml
Servers | OFF_VOICEMAIL_PREVIEW_PARTNER | ![voicemail_preview_partner](/office2014/Servers/voicemail_preview_partner.png?raw=true) | Servers/voicemail_preview_partner.puml
Servers | OFF_WEB_SERVER | ![web_server](/office2014/Servers/web_server.png?raw=true) | Servers/web_server.puml
Servers | OFF_WEB_SERVER_BLUE | ![web_server_blue](/office2014/Servers/web_server_blue.png?raw=true) | Servers/web_server_blue.puml
Servers | OFF_WEB_SERVER_GHOSTED | ![web_server_ghosted](/office2014/Servers/web_server_ghosted.png?raw=true) | Servers/web_server_ghosted.puml
Servers | OFF_WEB_SERVER_GREEN | ![web_server_green](/office2014/Servers/web_server_green.png?raw=true) | Servers/web_server_green.puml
Servers | OFF_WEB_SERVER_ORANGE | ![web_server_orange](/office2014/Servers/web_server_orange.png?raw=true) | Servers/web_server_orange.puml
Servers | OFF_WINDOWS_ROUTER | ![windows_router](/office2014/Servers/windows_router.png?raw=true) | Servers/windows_router.puml
Servers | OFF_WINDOWS_SERVER | ![windows_server](/office2014/Servers/windows_server.png?raw=true) | Servers/windows_server.puml
Services | OFF_3RD_PARTY_SERVICE | ![3rd_party_service](/office2014/Services/3rd_party_service.png?raw=true) | Services/3rd_party_service.puml
Services | OFF_ACCESS_SERVICES | ![access_services](/office2014/Services/access_services.png?raw=true) | Services/access_services.puml
Services | OFF_BUSINESS_CONNECTIVITY_SERVICES | ![business_connectivity_services](/office2014/Services/business_connectivity_services.png?raw=true) | Services/business_connectivity_services.puml
Services | OFF_CALL_ADMISSION_CONTROL_SERVICE | ![call_admission_control_service](/office2014/Services/call_admission_control_service.png?raw=true) | Services/call_admission_control_service.puml
Services | OFF_CENTRAL_MANAGEMENT_SERVICE | ![central_management_service](/office2014/Services/central_management_service.png?raw=true) | Services/central_management_service.puml
Services | OFF_CONFERENCE_ANNOUNCEMENT_SERVICE | ![conference_announcement_service](/office2014/Services/conference_announcement_service.png?raw=true) | Services/conference_announcement_service.puml
Services | OFF_DEVICE_UPDATE_SERVICE | ![device_update_service](/office2014/Services/device_update_service.png?raw=true) | Services/device_update_service.puml
Services | OFF_EMAIL_SERVICE | ![email_service](/office2014/Services/email_service.png?raw=true) | Services/email_service.puml
Services | OFF_EXCEL_SERVICES | ![excel_services](/office2014/Services/excel_services.png?raw=true) | Services/excel_services.puml
Services | OFF_FEDERATION_SERVICE | ![federation_service](/office2014/Services/federation_service.png?raw=true) | Services/federation_service.puml
Services | OFF_LYNC_STORAGE_SERVICE | ![lync_storage_service](/office2014/Services/lync_storage_service.png?raw=true) | Services/lync_storage_service.puml
Services | OFF_LYNC_WEB_APP_CLIENT | ![lync_web_app_client](/office2014/Services/lync_web_app_client.png?raw=true) | Services/lync_web_app_client.puml
Services | OFF_MOBILITY_SERVICE | ![mobility_service](/office2014/Services/mobility_service.png?raw=true) | Services/mobility_service.puml
Services | OFF_NETWORK_FILE_SHARE_SERVICE | ![network_file_share_service](/office2014/Services/network_file_share_service.png?raw=true) | Services/network_file_share_service.puml
Services | OFF_ONLINE_HOSTED_SERVICES | ![online_hosted_services](/office2014/Services/online_hosted_services.png?raw=true) | Services/online_hosted_services.puml
Services | OFF_OUTLOOK_WEB_APP | ![outlook_web_app](/office2014/Services/outlook_web_app.png?raw=true) | Services/outlook_web_app.puml
Services | OFF_POWERPOINT_AUTOMATION_SERVICES | ![powerpoint_automation_services](/office2014/Services/powerpoint_automation_services.png?raw=true) | Services/powerpoint_automation_services.puml
Services | OFF_PUSH_NOTIFICATION_SERVICE | ![push_notification_service](/office2014/Services/push_notification_service.png?raw=true) | Services/push_notification_service.puml
Services | OFF_REGISTRAR_SERVICE | ![registrar_service](/office2014/Services/registrar_service.png?raw=true) | Services/registrar_service.puml
Services | OFF_RESPONSE_GROUP_SERVICE | ![response_group_service](/office2014/Services/response_group_service.png?raw=true) | Services/response_group_service.puml
Services | OFF_SKYPE_FOR_BUSINESS_STORAGE_SERVICE | ![skype_for_business_storage_service](/office2014/Services/skype_for_business_storage_service.png?raw=true) | Services/skype_for_business_storage_service.puml
Services | OFF_USER_SERVICES | ![user_services](/office2014/Services/user_services.png?raw=true) | Services/user_services.puml
Services | OFF_VERIFICATION_SERVICE | ![verification_service](/office2014/Services/verification_service.png?raw=true) | Services/verification_service.puml
Services | OFF_VISIO_SERVICES | ![visio_services](/office2014/Services/visio_services.png?raw=true) | Services/visio_services.puml
Services | OFF_WEB_SERVICES | ![web_services](/office2014/Services/web_services.png?raw=true) | Services/web_services.puml
Services | OFF_WORD_AUTOMATION_SERVICES | ![word_automation_services](/office2014/Services/word_automation_services.png?raw=true) | Services/word_automation_services.puml
Services | OFF_XMPP_SERVICE | ![xmpp_service](/office2014/Services/xmpp_service.png?raw=true) | Services/xmpp_service.puml
Sites | OFF_ACCESS_SERVICES | ![access_services](/office2014/Sites/access_services.png?raw=true) | Sites/access_services.puml
Sites | OFF_BLOG_SITE | ![blog_site](/office2014/Sites/blog_site.png?raw=true) | Sites/blog_site.puml
Sites | OFF_BUSINESS_CONNECTIVITY_SERVICES | ![business_connectivity_services](/office2014/Sites/business_connectivity_services.png?raw=true) | Sites/business_connectivity_services.puml
Sites | OFF_EXCEL_SERVICES | ![excel_services](/office2014/Sites/excel_services.png?raw=true) | Sites/excel_services.puml
Sites | OFF_MEETING_WORKSPACE_SITE | ![meeting_workspace_site](/office2014/Sites/meeting_workspace_site.png?raw=true) | Sites/meeting_workspace_site.puml
Sites | OFF_MY_SITE | ![my_site](/office2014/Sites/my_site.png?raw=true) | Sites/my_site.puml
Sites | OFF_POWERPOINT_AUTOMATION_SERVICES | ![powerpoint_automation_services](/office2014/Sites/powerpoint_automation_services.png?raw=true) | Sites/powerpoint_automation_services.puml
Sites | OFF_PUBLISH | ![publish](/office2014/Sites/publish.png?raw=true) | Sites/publish.puml
Sites | OFF_SITE_COLLECTION | ![site_collection](/office2014/Sites/site_collection.png?raw=true) | Sites/site_collection.puml
Sites | OFF_SITE_SHARED | ![site_shared](/office2014/Sites/site_shared.png?raw=true) | Sites/site_shared.puml
Sites | OFF_SITE_TEAM | ![site_team](/office2014/Sites/site_team.png?raw=true) | Sites/site_team.puml
Sites | OFF_SUBSITE | ![subsite](/office2014/Sites/subsite.png?raw=true) | Sites/subsite.puml
Sites | OFF_SUBSITE_BLUE | ![subsite_blue](/office2014/Sites/subsite_blue.png?raw=true) | Sites/subsite_blue.puml
Sites | OFF_SUBSITE_GHOSTED | ![subsite_ghosted](/office2014/Sites/subsite_ghosted.png?raw=true) | Sites/subsite_ghosted.puml
Sites | OFF_SUBSITE_GREEN | ![subsite_green](/office2014/Sites/subsite_green.png?raw=true) | Sites/subsite_green.puml
Sites | OFF_SUBSITE_ORANGE | ![subsite_orange](/office2014/Sites/subsite_orange.png?raw=true) | Sites/subsite_orange.puml
Sites | OFF_UPGRADE_SITE | ![upgrade_site](/office2014/Sites/upgrade_site.png?raw=true) | Sites/upgrade_site.puml
Sites | OFF_VISIO_SERVICES | ![visio_services](/office2014/Sites/visio_services.png?raw=true) | Sites/visio_services.puml
Sites | OFF_WEBSITE | ![website](/office2014/Sites/website.png?raw=true) | Sites/website.puml
Sites | OFF_WEBSITE_PUBLIC | ![website_public](/office2014/Sites/website_public.png?raw=true) | Sites/website_public.puml
Sites | OFF_WIKI_SITE | ![wiki_site](/office2014/Sites/wiki_site.png?raw=true) | Sites/wiki_site.puml
Sites | OFF_WORD_AUTOMATION_SERVICES | ![word_automation_services](/office2014/Sites/word_automation_services.png?raw=true) | Sites/word_automation_services.puml
Users | OFF_ADMINISTRATOR | ![administrator](/office2014/Users/administrator.png?raw=true) | Users/administrator.puml
Users | OFF_APPROVER | ![approver](/office2014/Users/approver.png?raw=true) | Users/approver.puml
Users | OFF_CALL_CENTER_AGENT | ![call_center_agent](/office2014/Users/call_center_agent.png?raw=true) | Users/call_center_agent.puml
Users | OFF_COMMUNICATIONS | ![communications](/office2014/Users/communications.png?raw=true) | Users/communications.puml
Users | OFF_CONFERENCING_ATTENDANT | ![conferencing_attendant](/office2014/Users/conferencing_attendant.png?raw=true) | Users/conferencing_attendant.puml
Users | OFF_CREDENTIALS | ![credentials](/office2014/Users/credentials.png?raw=true) | Users/credentials.puml
Users | OFF_CSV_FILE | ![csv_file](/office2014/Users/csv_file.png?raw=true) | Users/csv_file.puml
Users | OFF_DISTRIBUTION_GROUP | ![distribution_group](/office2014/Users/distribution_group.png?raw=true) | Users/distribution_group.puml
Users | OFF_DYNAMIC_DISTRIBUTION_GROUP | ![dynamic_distribution_group](/office2014/Users/dynamic_distribution_group.png?raw=true) | Users/dynamic_distribution_group.puml
Users | OFF_MAIL_USER | ![mail_user](/office2014/Users/mail_user.png?raw=true) | Users/mail_user.puml
Users | OFF_MEETING | ![meeting](/office2014/Users/meeting.png?raw=true) | Users/meeting.puml
Users | OFF_MOBILE_USER | ![mobile_user](/office2014/Users/mobile_user.png?raw=true) | Users/mobile_user.puml
Users | OFF_ONLINE_USER | ![online_user](/office2014/Users/online_user.png?raw=true) | Users/online_user.puml
Users | OFF_ON_PREMISES_USER | ![on_premises_user](/office2014/Users/on_premises_user.png?raw=true) | Users/on_premises_user.puml
Users | OFF_OUTLOOK_USER | ![outlook_user](/office2014/Users/outlook_user.png?raw=true) | Users/outlook_user.puml
Users | OFF_RESPONSE_GROUP | ![response_group](/office2014/Users/response_group.png?raw=true) | Users/response_group.puml
Users | OFF_RESPONSE_GROUP_SERVICE | ![response_group_service](/office2014/Users/response_group_service.png?raw=true) | Users/response_group_service.puml
Users | OFF_ROLE_GROUP | ![role_group](/office2014/Users/role_group.png?raw=true) | Users/role_group.puml
Users | OFF_SKYPE_COMMERCIAL_USER | ![skype_commercial_user](/office2014/Users/skype_commercial_user.png?raw=true) | Users/skype_commercial_user.puml
Users | OFF_SKYPE_FOR_BUSINESS_USER | ![skype_for_business_user](/office2014/Users/skype_for_business_user.png?raw=true) | Users/skype_for_business_user.puml
Users | OFF_TENANT_ADMIN | ![tenant_admin](/office2014/Users/tenant_admin.png?raw=true) | Users/tenant_admin.puml
Users | OFF_UM_ENABLED_USER | ![um_enabled_user](/office2014/Users/um_enabled_user.png?raw=true) | Users/um_enabled_user.puml
Users | OFF_UNIVERSAL_SECURITY_GROUP | ![universal_security_group](/office2014/Users/universal_security_group.png?raw=true) | Users/universal_security_group.puml
Users | OFF_USER | ![user](/office2014/Users/user.png?raw=true) | Users/user.puml
Users | OFF_USERS | ![users](/office2014/Users/users.png?raw=true) | Users/users.puml
Users | OFF_USERS_BLUE | ![users_blue](/office2014/Users/users_blue.png?raw=true) | Users/users_blue.puml
Users | OFF_USERS_GHOSTED | ![users_ghosted](/office2014/Users/users_ghosted.png?raw=true) | Users/users_ghosted.puml
Users | OFF_USERS_GREEN | ![users_green](/office2014/Users/users_green.png?raw=true) | Users/users_green.puml
Users | OFF_USERS_ORANGE | ![users_orange](/office2014/Users/users_orange.png?raw=true) | Users/users_orange.puml
Users | OFF_USERS_TWO | ![users_two](/office2014/Users/users_two.png?raw=true) | Users/users_two.puml
Users | OFF_USERS_TWO_BLUE | ![users_two_blue](/office2014/Users/users_two_blue.png?raw=true) | Users/users_two_blue.puml
Users | OFF_USERS_TWO_GHOSTED | ![users_two_ghosted](/office2014/Users/users_two_ghosted.png?raw=true) | Users/users_two_ghosted.puml
Users | OFF_USERS_TWO_GREEN | ![users_two_green](/office2014/Users/users_two_green.png?raw=true) | Users/users_two_green.puml
Users | OFF_USERS_TWO_ORANGE | ![users_two_orange](/office2014/Users/users_two_orange.png?raw=true) | Users/users_two_orange.puml
Users | OFF_USER_ACCOUNTS | ![user_accounts](/office2014/Users/user_accounts.png?raw=true) | Users/user_accounts.puml
Users | OFF_USER_BLUE | ![user_blue](/office2014/Users/user_blue.png?raw=true) | Users/user_blue.puml
Users | OFF_USER_EXTERNAL | ![user_external](/office2014/Users/user_external.png?raw=true) | Users/user_external.puml
Users | OFF_USER_GHOSTED | ![user_ghosted](/office2014/Users/user_ghosted.png?raw=true) | Users/user_ghosted.puml
Users | OFF_USER_GREEN | ![user_green](/office2014/Users/user_green.png?raw=true) | Users/user_green.puml
Users | OFF_USER_ORANGE | ![user_orange](/office2014/Users/user_orange.png?raw=true) | Users/user_orange.puml
Users | OFF_USER_SERVICES | ![user_services](/office2014/Users/user_services.png?raw=true) | Users/user_services.puml
Users | OFF_USER_STORE | ![user_store](/office2014/Users/user_store.png?raw=true) | Users/user_store.puml
Users | OFF_WRITER | ![writer](/office2014/Users/writer.png?raw=true) | Users/writer.puml
