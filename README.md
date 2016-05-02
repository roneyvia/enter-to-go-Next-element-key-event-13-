# enter-to-go-Next-element-key-event-13-

```html
<table class="half">
    <tr>
        <td>Nome :</td>
        <td>
            <input class="inputs" name="ragsoc" type="text" id="ragsoc" value="" />
        </td>
        <td>Mnemo:</td>
        <td>
            <input class="inputs" name="mnemo" type="text" id="mnemo" value="" />
        </td>
        <td>Partita IVA :</td>
        <td>
            <input class="inputs" name="piva" type="text" id="piva" value="" />
        </td>
    </tr>
    <tr>
        <td>Nome :</td>
        <td>
            <input class="inputs" name="ragsoc" type="text" id="ragsoc" value="" />
        </td>
        <td>Mnemo:</td>
        <td>
            <input class="inputs" name="mnemo" type="text" id="mnemo" value="" />
        </td>
        <td>Partita IVA :</td>
        <td>
            <input class="inputs" name="piva" type="text" id="piva" value="" />
        </td0>
        
    </tr>
</table>
```


```javascript
  $('.inputs').keydown(function (e) {
         if (e.which === 13) {
             var index = $('.inputs').index(this) + 1;
             $('.inputs').eq(index).focus();
         }
     });
```

OR

```javascript
$('#inputform').on('keydown', 'input', function (event) {
    if (event.which == 13) {
        event.preventDefault();
        var $this = $(event.target);
        var index = parseFloat($this.attr('data-index'));
        $('[data-index="' + (index + 1).toString() + '"]').focus();
    }
});
``

