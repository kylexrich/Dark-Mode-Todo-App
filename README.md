# Dark Mode Todo App

A desktop to-do manager built with Java Swing. Track tasks with due dates, categories, and priorities, filter/auto-save, and enjoy a focused dark theme with subtle sound cues.

## Features
- Add tasks with name, due date, category, and priority; mark complete or delete.
- Smart filters: show overdue, due today/7 days/30 days, by priority/category, or completion status.
- View all tasks in a sortable list; toggle “match any” vs “match all” filters.
- Save/load task lists to JSON; optional auto-save toggle.
- Audio feedback for common actions (add, complete, delete, apply/remove filters).

## Tech stack
- **Language/UI:** Java 11+, Swing.
- **Data:** JSON persistence (org.json).
- **Build/Run:** IDE-friendly project (IntelliJ/Eclipse). Executable `TodoList.jar` included for quick runs.

## Project layout
```
/src/main/ui          # Main window, controller, entrypoint (Main.java)
/src/main/persistance # JSON loader/saver
/src/resources        # Icons, sounds, default data
/lib                  # Third-party jars (json, JUnit)
/docs                 # Archived course readme & artifacts (not required to run)
```

## Getting started
1. Install Java 11+ and an IDE (or use `javac`/`java`).
2. Clone the repo and ensure `lib/json-20200518.jar` is on the classpath.
3. Run the app:
   - **Fastest:**  
     ```bash
     java -jar TodoList.jar
     ```  
     (All features work; if file saving misbehaves on some platforms, run from source.)
   - **From source (IDE):** open the project, mark `lib/` jars as dependencies, and run `src/main/ui/Main.java`.
   - **From source (CLI example):**  
     ```bash
     javac -cp lib/json-20200518.jar -d out $(find src -name "*.java")
     java -cp out:lib/json-20200518.jar main.ui.Main
     ```

## Screenshots
- UI: https://i.imgur.com/1LwT9mT.png  
- UML: `UML_Design_Diagram.pdf` (in repo) or https://i.imgur.com/u5xbxxq.png

## Notes
- Default data lives in `src/resources/data/taskList.json`; saving overwrites this file when run from source.
- Sounds are in `src/resources/sfx/`; disable system audio if you prefer silent operation.
