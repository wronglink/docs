# Управление доступом

Пользователь Яндекс.Облака может выполнять только те операции над ресурсами, которые разрешены назначенными ему ролями. Пока у пользователя нет никаких ролей, почти все операции ему запрещены. Независимо от назначенных ролей, пользователь может просматривать справочные списки зон доступности и типов дисков.

Чтобы разрешить доступ к ресурсам компонента [!KEYREF instance-groups-name] сервиса [!KEYREF compute-full-name] (группам виртуальных машин, виртуальным машинам, дискам, образам и снимкам), назначьте пользователю нужные роли из приведенного ниже списка. На данный момент роль может быть назначена только на родительский ресурс (каталог или облако), роли которого наследуются вложенными ресурсами.

> [!NOTE]
>
> Подробнее о наследовании ролей читайте в разделе [[!TITLE]](../../resource-manager/concepts/resources-hierarchy.md#access-rights-inheritance) документации сервиса [!KEYREF resmgr-full-name].

## Назначение ролей

Чтобы назначить пользователю роль:

[!INCLUDE [grant-role-console.md](../../_includes/grant-role-console.md)]

## Роли

Ниже перечислены все роли, которые учитываются при проверке прав доступа в компоненте [!KEYREF instance-groups-name] сервиса [!KEYREF compute-short-name].

### Примитивные роли

Примитивные роли можно назначать на любой ресурс в любом сервисе.

#### [!KEYREF roles-owner]

Пользователь с ролью `[!KEYREF roles-owner]` может выполнять любые операции с ресурсами в облаке.

#### [!KEYREF roles-viewer]

Пользователь с ролью `[!KEYREF roles-viewer]` может просматривать информацию о ресурсах, например посмотреть список дисков или получить информацию о виртуальной машине.

#### [!KEYREF roles-editor]

Пользователь с ролью `[!KEYREF roles-editor]` может управлять любыми ресурсами, например создать виртуальную машину, остановить или запустить виртуальную машину, подключить или отключить диск.

Помимо этого роль `[!KEYREF roles-editor]` включает в себя все разрешения роли `[!KEYREF roles-viewer]`.

#### [!KEYREF roles-admin]

Пользователь с ролью `[!KEYREF roles-admin]` может управлять правами доступа к ресурсам, например разрешить другим пользователям создавать виртуальные машины или просматривать информацию о них.

Помимо этого роль `[!KEYREF roles-admin]` включает в себя все разрешения роли `[!KEYREF roles-editor]`.