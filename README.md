# 🌸 WPF Flower Shop

Это десктопное приложение для управления **цветочным магазином**, разработанное на платформе **.NET с использованием WPF и паттерна MVVM**. Программа позволяет просматривать каталог цветов, оформлять заказы, управлять складом и вести клиентскую базу.

## 🌼 Основные функции

* Каталог цветов 
* Управление корзиной и оформление заказов
* Регистрация, авторизация и личный кабинет
* Админ-панель (добавление/удаление/редактирование цветов, управление заказами и пользователями)
* История заказов для клиентов

## 🛠️ Технологии

* **.NET 8+**
* **WPF** (MVVM архитектура)
* **Entity Framework Core**
* **SQL Server
* * **ICommand**, **ObservableCollection**, **DataBinding**

## 💻 Системные требования

* Windows 10 или выше
* .NET SDK 8.0 или выше
* Visual Studio 2022+
* SQL Server 
## 🚀 Установка и запуск

1. **Клонируйте проект:**

   ```bash
   git clone https://github.com/your-username/wpf-flower-shop.git
   cd wpf-flower-shop
   ```

2. **Откройте решение в Visual Studio**

3. **Настройте строку подключения к базе данных**

   Строка подключения задаётся напрямую в `ApplicationDbContext.cs`:

   ```csharp
   protected override void OnConfiguring(DbContextOptionsBuilder optionsBuilder)
   {
       if (!optionsBuilder.IsConfigured)
       {
           optionsBuilder.UseSqlServer("Server=localhost;Database=FlowerShopDb;Trusted_Connection=True;");
       }
   }
   ```

4. **Примените миграции (если используются):**

   ```bash
   dotnet ef database update
   ```

5. **Запустите приложение**

   Нажмите `F5` или выберите пункт `Start` в Visual Studio.

## 🧪 Тестирование

```bash
dotnet test
```

## 📂 Структура проекта

```
/Models              - модели данных (Flower, Order, User и др.)
/ViewModels          - логика взаимодействия UI
/Views               - XAML-интерфейсы (главная, корзина, заказ)
/Services            - работа с БД и бизнес-логика
/ApplicationDbContext.cs - EF Core контекст с настройкой строки подключения
/App.xaml            - глобальные стили и ресурсы
/MainWindow.xaml     - стартовое окно
```

## 📄 Лицензия

Проект распространяется под лицензией MIT. См. файл [LICENSE](./LICENSE).

