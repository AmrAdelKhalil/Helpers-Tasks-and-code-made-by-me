# Helpers-Tasks-and-code-made-by-me
This repository was made to add snippets of codes that may be interesting for me and other people.

#How should you deal with the repo
All you have to do is include the file as it says in its description below.

# What is in this repo right now?
**Service.rake:**

This file is made for people who are like to work with `service object` pattern, I noticed that I was creating files by hand which
is something takes time, So with this rake you can save your time.

**Steps** to make it works:

1- download this file

2- include it inside `lib/task` for your rails project

**HOW TO USE IT?**

    rake service:install
    
this gonna make directory under `/app` called `services`

    rake service:create_service['<path_to_service_camel_cased_name>']
    
for example:

    rake service:create_service['CreateUser']
    
this gonna create file in path `app/services/create_user.rb` that includes a content like this.

    class CreateUser
    end
    
another example:

    rake service:create_service['admin/CreateUser']
    
this gonna create file in path `app/services/admin/create_user.rb` that includes a content like this.

    module Admin
    class CreateUser
    end
    end
