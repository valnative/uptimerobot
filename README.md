# Репозиторій буде доповнено згодом

# DevOps та Kubernetes. Практичний інтенсив
## Модуль 5. Kubernetes в дії
### Завдання на перевірку

Ваша команда оформила підписку на моніторинговий сервіс Uptime Robot.

Це надає можливість користувачам відстежувати статус в реальному часі.

Приклад Status Page https://status.uptimerobot.com

Вам надано інструкцію по заведенню на моніторинг ваших ресурсів.

To set up monitoring using Uptime Robot:

Log in to your Uptime Robot account or create a new account if you don't have one already.
Once logged in, navigate to the dashboard or main menu.
Look for the option to add a new monitor and click on it.
Select the "Keyword" monitor type from the available options.
Provide a friendly name or label for the monitor to easily identify it.
Enter the specific keyword or phrase that you want to monitor in the provided field.
Choose the appropriate settings for the monitoring interval and timeout duration.
Specify any additional advanced settings or alert configurations as needed.
Save the monitor settings to activate it.
Uptime Robot will now start monitoring the specified keyword on the designated website or page.
That's it! By setting up a Keyword monitor in Uptime Robot, you can receive alerts or notifications whenever the specified keyword is not found or present on the monitored webpage. This can help you ensure the availability and proper functioning of critical content or elements on your website or online service.

Для реалізації цієї задачі вам необхідно  виконати два завдання.

Важливе зауваження! При розгортанні реальної інфраструктури, особливо з використанням GCP free credits, потрібно приділяти увагу затратам часу та коштів. Рекомендуємо виконувати завдання послідовно без відтермінування в часі, оскільки це допоможе заощадити ресурси. Якщо ви не впевнені, що зможете виконати два завдання одночасно, рекомендуємо розгортати кластери під кожне завдання окремо. Після успішної перевірки, не забудьте видалити кластер командою gcloud

Завдання 1 
1 спроба, 5 балів

1. Розгорніть Kubernetes кластер на Google Cloud за допомогою gcloud cli

2. Після отримання доступу до кластеру, створіть deployment v1.0.0 що повертає версію “Version: 1.0.0”

3. Налаштуйте сервіс типу LoadBalancer та отримайте IP-адресу

4. Налаштуйте Monitor Type Keyword у Uptime Robot вказавши IP-адресу балансера та Keyword “Version: 1.0.0”

5. Моніторингова система перевірить в реальному часі доступність першої версії

6. Налаштуйте публічну status page додавши до неї перший Monitoring

Завдання 2
1 спроба, 5 балів

7. Наступним кроком внесіть зміни у програму, збілдайте та запуште нову версію контейнеру у контейнер реєстр

8. Створить новий деплоймент з версію образу v2.0.0

9. Переведіть трафік з першої на другу версію методами: Canary (25%) та Blue-Green (100%) Deployment

10. По завершенню тестування, залишіть активною v2.0.0 на 100%

11. Налаштуйте Monitor Type Keyword у Uptime Robot вказавши IP-адресу балансера та Keyword “Version: 2.0.0”

12. Моніторингова система перевірить в реальному часі доступність другої версії

13. Налаштуйте публічну status page додавши до неї другий Monitoring

Надішліть у відповідь посилання на Status Page з історією перевірок.

Приклад формату відповіді: https://stats.uptimerobot.com/Zm6V0FMoO7
