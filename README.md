ActsAsTaggableOnActiveRecordRelation
====================================

Allow you to bulk add/remove tags directly on an ActiveRecord::Relation


How to use it
-------------

If you are using *Rails 3* Just put the .rb file it in your */lib* folder

```ruby
# Our ActiveRecord::Relation
clients = Client.where('created_at > ?', Time.now - 2.months)
# Our tags
tags_to_add = ['here','a','bunch','of','tags']
tags_to_remove = ['useless','now']
# Adding and removing tags
# (You can specify the tagging context as a second parameter) 
clients.add_tags(tags_to_add).remove_tags(tags_to_add, 'jobs')
```

Note:
-----
Works on MySQL databases