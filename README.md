# Odoo 12.0 - Technical Training
=======
# View Inheritance

## Goal

Odoo provides an *inheritance* mechanism to extend a view in a modular way. The
view extension describes modifications of the XML of the extended view. It can,
for instance, add elements, modify elements or modify element attributes. It
usually complements model extensions.

The purpose of this module is to learn this inheritance mechanism.


## Requirements

- [Models, Fields and Relations]https://github.com/odoo/technical-training/tree/12.0-01-models)
- [Basic Views]https://github.com/odoo/technical-training/tree/12.0-03-views)
- [Model Inheritance]https://github.com/odoo/technical-training/tree/12.0-04-model-inheritance)


## Problem 1: Instructors (OpenAcademy)

In the openacademy module, we have added fields on the contacts (model `res.partner`).
The boolean field `instructor` distinguishes between instructors and other contacts,
and a read-only field shows the sessions attended by a given contact.
For now we've created a new view. The more efficient way would be to have only "one"
view per type of view for the res.partner model.

## Problem 2: Library Management

In the previous training module, we added a specific data model for book copies.
Modify the form view of that model to make it inherit from the form view of the
book model.


## Resources

### Reference

* [View Inheritance](http://www.odoo.com/documentation/12.0/reference/views.html#inheritance)
* [Online Tutorial](http://www.odoo.com/documentation/12.0/howtos/backend.html#view-inheritance)

### Code Sample

* [Add elements to a form view](https://github.com/odoo/odoo/blob/76c443eda331b75bf5dfa7ec22b8eb22e1084343/addons/account/views/product_view.xml#L10)
* [Add elements inside another](https://github.com/odoo/odoo/blob/76c443eda331b75bf5dfa7ec22b8eb22e1084343/addons/account/views/partner_view.xml#L98)
* [Replace an element by another](https://github.com/odoo/odoo/blob/76c443eda331b75bf5dfa7ec22b8eb22e1084343/addons/product/views/product_views.xml#L139)
* [Modify element attributes](https://github.com/odoo/odoo/blob/76c443eda331b75bf5dfa7ec22b8eb22e1084343/addons/product/views/product_views.xml#L277)
