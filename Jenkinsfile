
// Объявление pipeline
pipeline { 
    // Используем любой свободный Jenkins агент
    agent any
    environment { // Переменные среды
        CI = 'true' // Не требовать input от пользователя
    }
    stages { // Указываем набор этапов по deployment
            stage('Build') { // Создаем этап с названием Build
                steps { // Создаем шаги внутри этапа
                    sh 'docker build -t clinics:latest .' // Вызов команды bash
                }
            }
     }
}
