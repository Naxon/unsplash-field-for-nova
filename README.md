# Unsplash field for Nova

This custom field has the ability to fetch and display an image from Unsplash in Laravel Nova.

### Installation

```shell
composer require simonbarrettact/unsplash
```

The Unsplash field requires you to set up an Unsplash access key.

Get your Unsplash access key from [the develop dashboard](https://unsplash.com/developers) after creating an app with them.

Once you have doner that, add the following line, containing your key, to your `.env` file.

```
UNSPLASH_ACCESS_KEY=<your access key>
```

### Usage

Before using the field it will be necessary to add a column to your table.

```php
/** * Run the migrations. 
 * 
 * @return void 
 */
 public function up()
 {    
 	Schema::table('my_table', function (Blueprint $table) {
 	   $table->string('unsplash_id', 20);
 	});
 }
```
