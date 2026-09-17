# Title: Templating-with-go

Date:2025-09-15

---

Page specific template structs. I can use a base template struct, that can be shared with page specific templates.

```
type BaseTemplateData struct {
    IsAuthenticated bool
    Merchant       *models.Merchant  // Current logged-in merchant
    Error          string
    Token          string
}

type HomePageData struct {
    BaseTemplateData
    Products  []*models.Product
    Merchants []*models.Merchant
    Services  []*models.Service
}

```

## UP

## DOWN
