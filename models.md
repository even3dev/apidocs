# 🦴 Models

### ‌CheckinAttendee

| Nome da propriedade | Tipo da propriedade | Descrição                                             |
| ------------------- | ------------------- | ----------------------------------------------------- |
| checkin\_code       | string              | Número de inscrição do participante em um evento      |
| checkin             | int                 | Flag para credenciar ou não credenciar o participante |
| checkin\_date       | datetime            | Data de credenciamento                                |

​‌

### CheckinSession

| Nome da propriedade | Tipo da propriedade | Descrição                                                          |
| ------------------- | ------------------- | ------------------------------------------------------------------ |
| id\_attendees       | int                 | Id do participante                                                 |
| id\_session         | int                 | Id da atividade                                                    |
| checkin             | int                 | Flag para credenciar ou não credenciar o participante na atividade |
| checkin\_date       | datetime            | Data de credenciamento                                             |
