## User

| Column     | Type   | Options     |
| ---------- | ------ | ----------- |
| Email      | String | null: false |
| Password   | String | null: false |
| Name       | String | null: false |
| Profile    | String | null: false |
| Occupation | String | null: false |
| Position   | String | null: false |

### Association
-has_many :prototypes
-has_many :comments

## Comments

| Column    | Type       | Options     |
| --------- | ---------- | ----------- |
| Text      | text       | null: false |
| User      | references |             |
| Prototype | references |             |

### Association
-belongs_to :user
-belongs_to :prototype

## Prototypes

| Column     | Type          | Options     |
| ---------- | ------------- | ----------- |
| Title      | string        | null: false |
| Catch_copy | text          | null: false |
| Concept    | text          | null: false |
| Image      | activeStorage |             |
| User       | references    |             |

### Association 
-belongs_to :user
-has_many   :comments
