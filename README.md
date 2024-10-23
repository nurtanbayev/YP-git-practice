git init - инициирует git репозиторий
git add - добавляет файл в staged area
git commit -m - добавляет файл в локальный репозиторий с сообщением
git status - показывает статус файлов

```mermaid

config:
    look: handDrawn
    theme: neutral

graph TD;
    A[Working tree] -- git add --> B[Staging area]
    B -- git commit --> C[Local branch]
    C -- git push --> D[Remote branch]
    D -- git fetch --> E[Remote tracking ref]
    D -- git pull --> A
    C -- git checkout --> A
    E -- git merge/rebase --> A
```