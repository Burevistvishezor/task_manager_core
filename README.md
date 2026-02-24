# task_manager_core
from dataclasses import dataclass
from enum import Enum
from typing import Optional

# Определяем перечисление для статуса задачи
class TaskStatus(Enum):
    TODO = "to do"
    IN_PROGRESS = "in progress"
    DONE = "done"
    CANCELLED = "cancelled"

# Класс User с атрибутами: id, name, email
@dataclass
class User:
    id: int
    name: str
    email: str

# Класс Task с атрибутами: id, title, status (enum)
@dataclass
class Task:
    id: int
    title: str
    status: TaskStatus

# Пример использования классов
if __name__ == "__main__":
    # Создаем объект User
    user = User(id=1, name="John Doe", email="john.doe@example.com")
    print(user)  # User(id=1, name='John Doe', email='john.doe@example.com')

    # Создаем объект Task
    task = Task(id=1, title="Complete the project", status=TaskStatus.IN_PROGRESS)
    print(task)  # Task(id=1, title='Complete the project', status=<TaskStatus.IN_PROGRESS: 'in progress'>)
@dataclass
class Task:
    id: int
    title: str
    status: TaskStatus
