(multilinguela)[https://www.accordbox.com/blog/how-support-multi-language-wagtail-cms/]

## error NoneType' object has no attribute

    from wagtail.core.models import Page
    pages = Page.objects.all()
    for p in pages:
        if not p.specific_class:
            p.delete()
