== README

#  table definition

[Table definition](https://docs.google.com/spreadsheets/d/1ZRFdFiNkgUpKh1rE6lYOJDXIms4hs_rcGXXeLwV2Su0/edit?usp=sharing)

* Users
   * has_many | prototypes
   * has_many | likes
   * has_many | comments

* Tags
   * has_many | prototypes(through)tagging

* Prototypes
   * has_many | tags(through)tagging
   * has_many | comments
   * has_many | likes
   * belongs_to | user

* Likes
   * belongs_to | prototype
   * belongs_to | user

* Comments
  * belongs_to | user
  * belongs_to | prototypes