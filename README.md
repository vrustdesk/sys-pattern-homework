Домашнее задание по лекции "GitLab" Иванов Владислав

Задание 1
Что нужно сделать:

Разверните GitLab локально, используя Vagrantfile и инструкцию, описанные в этом репозитории.
Создайте новый проект и пустой репозиторий в нём.
Зарегистрируйте gitlab-runner для этого проекта и запустите его в режиме Docker. Раннер можно регистрировать и запускать на той же виртуальной машине, на которой запущен GitLab.
В качестве ответа в репозиторий шаблона с решением добавьте скриншоты с настройками раннера в проекте.

Задание 2
Что нужно сделать:

Запушьте репозиторий на GitLab, изменив origin. Это изучалось на занятии по Git.
Создайте .gitlab-ci.yml, описав в нём все необходимые, на ваш взгляд, этапы.
В качестве ответа в шаблон с решением добавьте:

файл gitlab-ci.yml для своего проекта или вставьте код в соответствующее поле в шаблоне;
скриншоты с успешно собранными сборками.
---

РЕШЕНИЕ

Задание 1

установил и запустил Gitlub image
![image](https://github.com/user-attachments/assets/b86ad414-e1dc-4852-9462-3892c283996d)

Создал проект image
![image](https://github.com/user-attachments/assets/61a430a9-f35c-4dc1-87d8-1473df409f84)

Зарегистрировал gitlab-runner для этого проекта и запустил его в режиме Docker image
![image](https://github.com/user-attachments/assets/d5f79c6f-9205-4531-ad18-338138f266a0)





   Задание 2

Запушил репозиторий на GitLab, изменив origin image
![image](https://github.com/user-attachments/assets/e30a3561-8a52-41cf-82ea-914dcdd1c082)

Содержимое файла .gitlab-ci.yml:

stages:
  - test
  - build

test:
  stage: test
  image: golang:1.17
  script: 
   - go test .

build:
  stage: build
  image: docker:latest
  script:
   - docker build .

Так же прикладываю файл в решение

Скриншоты с собранными сборками image
![image](https://github.com/user-attachments/assets/71b59e71-61da-48da-bdf5-164e88786324)




