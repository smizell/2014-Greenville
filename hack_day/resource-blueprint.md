# ToDo API
Currently a WIP

## API Entry Point
[Home@default][]

## Resource Home

### Affordances
+ userCreate ... Create a new user and signin
    + Traits
        + profile_type: unsafe

    + Attributes
        + userName (string) ... Username of User
            + Traits
                + profile_type: semantic

        + password (string) ... Account Password
            + Traits
                + profile_type: semantic

        + givenName ... Given Name of User
            + Traits
                + profile_type: semantic

        + familyName ... Family Name of User
            + Traits
                + profile_type: semantic

        + avatarUrl ... Avatar URL
            + Traits
                + profile_type: semantic

### Attributes
+ id ... User ID
    + Traits
        + profile_type: semantic

+ userName ... Username of User
    + Traits
        + profile_type: semantic

+ givenName ... Given Name of User
    + Traits
        + profile_type: semantic

+ familyName ... Family Name of User
    + Traits
        + profile_type: semantic

+ avatarUrl ... Avatar URL

+ dateCreated ... Date Created
    + Traits
        + profile_type: semantic

+ dateUpdated ... Date Updated
    + Traits
        + profile_type: semantic

### Affordances
+ show
    + Traits
        + profile_type: safe

+ edit
    + Traits
        + profile_type: unsafe

+ delete
    + Traits
        + profile_type: idempotent

## Resource Categories

### Attributes
+ items (array) ... An array of embedded Category items
    + Traits
        + profile_type: semantic
    + Embedded Entities
        + [Category][]

### Affordances
+ create ... Create a new category and append to category collection
    + Traits
        + profile_type: unsafe

    + Attributes
        + title (string) ... Name of Category
            + Traits
                + profile_type: semantic

## Resource Category

### Attributes
+ id ... Category ID
    + Traits
        + profile_type: semantic

+ title ... Name of Category
    + Traits
        + profile_type: semantic

+ dateCreated ... Date Created
    + Traits
        + profile_type: semantic

+ dateUpdated ... Date Updated
    + Traits
        + profile_type: semantic

+ user ... Creator of Category
    + Traits
        + profile_type: semantic

### Affordances
+ show
+ categories

## Resource Todos

### Attributes
+ items (array) ... An array of embedded todos
    + Traits
        + profile_type: semantic

    + Embedded Entities
        + [Todo][]

### Affordances
+ create ... Create a new to-do and append to to-do collection
    + Traits
        + profile_type: unsafe

    + Attributes
        + title (string) ... Name of Todo
            + Traits
                + profile_type: semantic
        + dueDate () ... Due date of Todo
            + Traits
                + profile_type: semantic
        + notes (string) ... Additional text about the item
            + Traits
                + profile_type: semantic
        + categories (array) ... Array of category titles
            + Traits
                + profile_type: semantic

## Resource Todo

### Attributes
+ id (number) ... Category ID
    + Traits
        + profile_type: semantic

+ title (string) ... Name of Category
    + Traits
        + profile_type: semantic

+ dueDate () ... Due date of Todo
    + Traits
        + profile_type: semantic

+ notes (string) ... Additional text about the item
    + Traits
        + profile_type: semantic

+ dateCreated ... Date Created
    + Traits
        + profile_type: semantic

+ dateUpdated ... Date Updated
    + Traits
        + profile_type: semantic

+ user ... Creator of Category
    + Traits
        + profile_type: semantic

+ categories (array) ... An array of embedded Category items
    + Traits
        + profile_type: semantic
    + Embedded Entities
        + [Category][]

### Affordances
+ show
    + Traits
        + profile_type: safe

+ edit
    + Traits
        + profile_type: idempotent

+ delete
    + Traits
        + profile_type: idempotent

+ todos
    + Traits
        + profile_type: safe

+ todoSend
    + Traits
        + profile_type: idempotent