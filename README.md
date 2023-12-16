# Отчёт по аналитической лабе №1
# Состав команды
* Калинин Артур К3222
* Волкович Кирилл К3222
* Суслопаров Виталий К3222
* Гаврилов Кирилл К3222
# Цель работы
Знакомство с облачными сервисами. Понимание уровней абстракции над инфраструктурой в облаке. Формирование понимания типов потребления сервисов в сервисной-модели. Сопоставление сервисов между разными провайдерами. Оценка возможностей миграции на отечественные сервисы.
# Дано
1. Слепок данных биллинга от провайдера после небольшой обработки в виде SQL-параметров. Символ % в начале/конце означает, что перед/после него может стоять любой набор символов.
2. Google с документациями провайдера
# Исходные данные
![Image alt](https://github.com/kirillvolkovich/anal-laba-1/blob/main/da.JPG)
# Описание сервисов
### Amazon FSx
Amazon FSx - это управляемый сервис файлового хранилища в облаке. Он предназначен для быстрого развертывания и масштабирования высокопроизводительных файловых систем для использования в облачных приложениях. Amazon FSx поддерживает различные протоколы доступа к файловым системам, такие как SMB (Server Message Block) для Windows и Lustre для Linux. С помощью фукнций резервного копирования, шифрования и интеграции с другими сервисами AWS, Amazon FSx обеспечивает удобное и надежное хранение данных для облачных приложений.
### Amazon Glacier
Amazon Glacier - это низкозатратный облачный сервис для долгосрочного хранения данных. Он предназначен для архивирования и долгосрочного хранения данных, которые не требуют частого доступа, но должны быть сохранены на долгий срок с возможностью восстановления в случае необходимости. Сервис предлагает высокую устойчивость данных и обеспечивает шифрование данных в покое, что делает его подходящим для различных областей, таких как хранение архивов, бэкапов и долгосрочного хранения данных.
### Amazon Guard Duty
Amazon Guard Duty - это облачный сервис безопасности, он использует машинное обучение и аналитику для поиска аномальной активности и возможных угроз безопасности в облаке. Сервис анализирует данные журналов, сетевую активность и другие источники информации, чтобы обнаруживать подозрительные действия, несанкционированный доступ и другие угрозы. После обнаружения проблемы, сервис предоставляет подробные отчеты и рекомендации по устранению уязвимостей.
### Amazon Inspector
Amazon Inspector -  это сервис безопасности, он предназначен для автоматической проверки безопасности приложений на соответствие стандартам безопасности и лучшим практикам. Сервис сканирует инфраструктуру и приложения на наличие уязвимостей, отслеживает изменения в безопасности и предоставляет рекомендации по улучшению безопасности. А также предоставляет отчеты о безопасности, которые помогут улучшить защиту облачного окружения.
### Amazon Amplify
Amazon Amplify -  это сервис, который позволяет разработчикам создавать современные веб- и мобильные приложения с использованием облачных возможностей. Сервис предоставляет набор инструментов для разработки, развертывания и управления приложениями, включая облачные услуги, мобильные уведомления, аутентификацию, хранение данных и многое другое. С помощью него разработчики могут ускорить процесс разработки приложений, используя готовые компоненты и упрощенные интеграции с облачными сервисами AWS.
### Amazon Backup
Amazon Backup - это сервис резервного копирования, он предназначен для создания и управления резервными копиями данных в облаке AWS, включая серверы, хранилища данных, базы данных и другие ресурсы. Сервис позволяет автоматизировать процесс создания резервных копий, управлять их хранением и восстановлением данных, что помогает обеспечить более надежную защиту информации и обеспечить бизнес-непрерывность в случае сбоев или потерь данных.
### Amazon DAX
Amazon DAX - это сервис кэширования для ускорения доступа к данным в облачной базе данных DynamoDB. Сервис предназначен для повышения производительности и отзывчивости приложений, использующих DynamoDB, путем предоставления высокоскоростного кэширования запросов к данным. Сервис автоматически обрабатывает кэширование, распределение запросов и управление кэшем, что позволяет улучшить производительность приложений и освободить нагрузку с облачной базы данных.
### Amazon DynamoDB
Amazon DynamoDB - это облачный сервис NoSQL базы данных. Он предназначен для создания гибких, высокодоступных и масштабируемых баз данных, которые могут обрабатывать большие объемы трафика и данных. Сервис позволяет легко хранить и манипулировать данными, предоставляя гибкость и масштабируемость, а также поддерживает автоматическое распределение и масштабирование нагрузки. Также поддерживает широкий спектр возможностей, включая автоматическое резервное копирование, мониторинг и управление данными, что позволяет разработчикам создавать надежные и масштабируемые облачные приложения.
### Amazon EKS
Amazon EKS - это управляемый сервис контейнеризации. Он позволяет развертывать, масштабировать и управлять приложениями на платформе Kubernetes в облаке AWS. Сервис упрощает процесс использования Kubernetes, предоставляя управляемый контрольный план и автоматизирующий задачи по развертыванию, масштабированию и обновлению кластеров Kubernetes. А также предоставляет встроенную интеграцию с другими сервисами AWS, обеспечивая безопасность, мониторинг и масштабируемость при работе с контейнеризированными приложениями.
### Amazon SageMaker
Amazon SageMaker - это управляемый сервис облачного машинного обучения. Сервис позволяет создавать, обучать и развертывать модели машинного обучения в облаке, обеспечивая интеграцию с другими сервисами AWS.Также предоставляет возможности для работы с различными типами моделей, автоматического масштабирования и упрощения процесса развертывания моделей в производственной среде. В сервис входят инструменты для анализа данных, разработки моделей, обучения, валидации и тестирования моделей, а также работы с ресурсами облака.

# Маппинг
| Amazon | Yandex Cloud |
|----------|----------|
| Amazon FSx | Yandex Managed Service for MongoDB |
| Amazon Glacier | Yandex Object Storage |
| Amazon Guard Duty | Нет точного аналога |
| Amazon Inspector | Нет точного аналога |
| Amazon Amplify | Нет точного аналога |
| Amazon Backup | Yandex Managed Service for Backup |
| Amazon DAX | Нет точного аналога |
| Amazon DynamoDB | Yandex Managed Service for YDB |
| Amazon EKS | Yandex Managed Service for Kubernetes |
| Amazon SageMaker | Yandex DataSphere |

# Итоговая таблица
![Image alt](https://github.com/kirillvolkovich/anal-laba-1/blob/main/itog1.JPG)
# Вывод
В результате выполнения лабораторной работы были проанализированы Amazon сервисы с использованием информации из официальной документации. После анализа была построена таблица, содержащая подробную информацию о сервисах Amazon, у каждого сервиса были заполнены элементы модели ATUM. Говоря об отечественных аналогах, можно сделать вывод, что полный переход затруднителен, у многих сервисов просто не оказалось отечественного аналога. Так, например, у сервисов Amazon Gurad Duty и Inspector не нашлось анлога в Yandex Cloud, однако все же есть несколько сервисов для защиты - Yandex Security Operations Center (SOC) и Yandex Managed Service for Security. Оба этих сервиса предназначены для мониторинга безопасности облачной инфраструктуры, обнаружения уязвимостей и анализа безопасности приложений, но мало чем схожи с сервисами от Amazon. Также в пример можно привести еще и Amazon Amplify, у Yandex есть похожий сервис - Yandex Mobile Solutions, который может предоставить определенные возможности для разработки и развертывания веб-приложений и мобильных приложений, но по прежнему отличается по функциональности от Amazon Amplify.
