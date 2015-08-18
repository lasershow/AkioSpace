== README

#  table definition

[Table definition](https://docs.google.com/spreadsheets/d/1ZRFdFiNkgUpKh1rE6lYOJDXIms4hs_rcGXXeLwV2Su0/edit?usp=sharing)

### Users

#### column

    column_name | column_date
    ------------|------------
    id | int(11)
    name | int(11)
    passward | int(11)
    nickname | string
    introduction | text
    created_at | datetime
    updated_at | datetime

#### association

   * has_many | prototypes
   * has_many | likes
   * has_many | comments

### Tags

#### column

   column_name | column_date
    ------------|------------
    id  | int(11)
    name | int(11)
    passward | int(11)
    nickname | string
    introduction | text
    created_at | datetime
    updated_at | datetime

#### association

   * has_many | prototypes(through)tagging

### Prototypes

#### column

    column_name | column_date
    ------------|------------
    id | int(11)
    user_id | int(11)
    tag_id | int(11)
    created_at | datetime
    updated_at | datetime

#### association

   * has_many | tags(through)tagging
   * has_many | comments
   * has_many | likes
   * belongs_to | user

### Likes

##### column

    column_name | column_date
    ------------|------------
    id | int(11)
    prototype_id | int(11)
    user_id | int(11)
    like | int(11)
    created_at | datetime
    updated_at | datetime

#### association

     * belongs_to | prototype
     * belongs_to | user

### Comments

#### column

    column_name | column_date
    ------------|------------
    id | int(11)
    user_id | int(11)
    prototype_id | int(11)
    coment | text
    created_at | datetime
    updated_at | datetime

#### association

    * belongs_to | user
    * belongs_to | prototypes

