
# Dimension Fieldtype

## What it does

This fieldtype let's you define 3 dimensions width / height / depth as integer.

### Output the values in templates

There's a property for each dimension

```
echo $page->fieldname->width;
echo $page->fieldname->height;
echo $page->fieldname->depth;
```

There's also support for a computed value of the volume. W*H*D. This will get stored additionally
to the database and updated every time a dimension value changed. So it can also be used in selectors for querying.

```
echo $page->fieldname->volume;
```

### Use in selectors strings

The dimensions can be used in selectors like:

`$pages->find("dimension.width=120");`

or

`$pages->find("dimension.height>=100, dimension.depth<120");`

or

`$pages->find("dimension.volue>=1000);`


## How to install

1. Download and place the module folder named "FieldtypeDimensions" in:
/site/modules/

2. In the admin control panel, go to Modules. At the bottom of the
screen, click the "Check for New Modules" button.

3. Now scroll to the FieldtypeDimension module and click "Install". The required InputfieldDimension will get installed automatic.

4. Create a new Field with the new "Dimension" Fieldtype.

## Support thread

[http://processwire.com/talk/topic/4081-fieldtypedimension/](http://processwire.com/talk/topic/4081-fieldtypedimension/)
