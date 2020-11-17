Here There is explanation of how to use "singular" and "plural" properly in Rails

The reverse of pluralize, returns the singular form of a word in a string.
- 'posts'.singularize            # => "post"
Rails can create the model, controller and view files associated with your application. The downside of using rails 

pluralize(count = nil, locale = :en) public
- Returns the plural form of the word in the string.

If the optional parameter count is specified, the singular form will be returned if count == 1. For any other value of count the plural will be returned.

If the optional parameter locale is specified, the word will be pluralized as a word of that language. By default, this parameter is set to :en. You must define your own inflection rules for languages other than English.

- 'post'.pluralize             # => "posts"

pluralize( 1, 'person' )
# => 1 person

pluralize( 2, 'person' )
# => 2 people

It is really very simple we have model name singular, table name plural but association can be singular or plural depends on how many records are associated. For eg. User has many books. We can find many books like => User.last.books It will return all the books. Book belongs to a user. We are defining a single user related with book. So Book.last.user
