---
title: Create a Model
---
## Create a Model

We need a **Schema** to build a **Model**. It defines the shape of a collection of MongoDB *i.e. The basic skeleton of a Collection.*
- Schemas can be simple or nested. Nested Schemas are usually used to store complex data.
- A model allows you to create instances of your objects, called **documents**.

> Create a Table having this prototype :

| Keys              |   Values          | 
| ------------------|:-----------------:| 
| size              | string [required] |
| woodtype          | string            |  
| Brands            | arrays of Strings |

- The *mongoose* package provides syntaxes for basic *schema types*. We can add more fields, validators like `required`, `unique` or set a default value by `default`.
> See the [mongoose docs](http://mongoosejs.com/docs/guide.html) for knowing everything.
```javascript
var Schema = mongoose.Schema;
var TableSchema = new Schema({size: {type:String, required: true}, woodType: String, Brands: [String]});
var table = mongoose.model('Table', TableSchema);
```

So, that's all required for creating a **Model**.
<!-- The article goes here, in GitHub-flavored Markdown. Feel free to add YouTube videos, images, and CodePen/JSBin embeds  -->
