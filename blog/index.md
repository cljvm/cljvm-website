title:  Blog
layout: blog.liquid
permalink: /blog/index.html
---

## My Blog

Welcome

// https://www.louisvuitton.cn/zhs-cn/products/pochette-accessoires-monogram-005656

```javascript
// 添加到购物车
$("#addToCartSubmit").click();

// 打开购物车
//$("#header-shoppingBag").click();

// 立即结账
$("#viewTaxesAndDetails").click();

// 产品型号
// $("#linkToProductPage_attributItem-M40712");
// 查看购物车中的产品
// var prod = $("[id^=linkToProductPage_attributItem]");
function removeProd() {
    var prod = $("[id^=remove_nvc]");
    prod.each(function(idx, item) {
        var myProds = ["M40712"];
        if(myProds.indexOf(item.getAttribute("data-sku")) == -1) {
            // 从购物车删除
            $(item).click();
            // todo 等待弹出
            $("#removeItemFromOrderSubmit").click()
        }
    });
}
function setQuy() {
    var prod = $("[id^=changeCommerceItemInput_nvc]");
    prod.each(function(idx, item) {
        var myProds = ["M40712"];
        if(myProds.indexOf(item.getAttribute("data-sku")) != -1) {
            // 设置数量1
            var $item = $(item);
            $item.val("1");
            $item.trigger("change");
        } else {
            removeProd();    
        }
    });
}
removeProd();
setQuy();

// 提交
$("#proceedToCheckoutButtonTop").click();
```
