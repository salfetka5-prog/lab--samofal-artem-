# Ініціалізація репозиторію
git init

# Створення develop-гілки
git checkout -b develop

# Створення фічі
git checkout -b feature/map-page
# ... код ...
git add .
git commit -m "Додано сторінку карти Mirage"
git checkout develop
git merge feature/map-page

# Створення релізу
git checkout -b release/v1.0.0
git tag v1.0.0
git checkout main
git merge release/v1.0.0
git push origin main --tags
