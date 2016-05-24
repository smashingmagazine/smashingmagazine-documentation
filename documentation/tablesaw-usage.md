# How to use Tablesaw in Smashing Magazine articles

## 1. Activate tablesaw.js

To use [Tablesaw](https://github.com/filamentgroup/tablesaw) in articles its script of the same name needs to be activated. In order to do this you will need to check the box inside the "Custom Post Options" (on `post.php` right under the textarea of your article) in the WordPress backend. Next to the checkbox you can read "Enable the tablesaw-JS for responsive tables"

![Enabling Tablesaw in the WordPress backend](/assets/tablesaw/tablesaw-usage-screen-01.png)

By doing so and saving your draft `tablesaw.js` and `jquery.js` will now be sent to the user when requesting your article.

## 2. Markup

Example Markup for a table with all needed attributes and values.

Give your table a class of `tablesaw`, the attribute/value combination of `data-tablesaw-mode="swipe"` and the boolean `data-tablesaw-minimap`. There were other options but this is the most handy and reliable one in the context of the design of Smashing Magazine.

In order to make the first column persistent you can add `data-tablesaw-priority="persist"` to the first `<th>` element in the `<thead>` element.

```
<table class="tablesaw" data-tablesaw-mode="swipe" data-tablesaw-minimap>
  <thead>
    <tr>
      <th data-tablesaw-priority="persist">Table Headline</th>
      <th>Table Headline</th>
      <th>Table Headline</th>
      <th>Table Headline</th>
      <th>Table Headline</th>
    </tr>
  </thead>
  <tbody>
    <tr>
      <td>First Row</td>
      <td>First Row</td>
      <td>First Row</td>
      <td>First Row</td>
      <td>First Row</td>
    </tr>
    <tr>
      <td>Second Row</td>
      <td>Second Row</td>
      <td>Second Row</td>
      <td>Second Row</td>
      <td>Second Row</td>
    </tr>
    <tr>
      <td>Third Row</td>
      <td>Third Row</td>
      <td>Third Row</td>
      <td>Third Row</td>
      <td>Third Row</td>
    </tr>
    <tr>
      <td>Fourth Row</td>
      <td>Fourth Row</td>
      <td>Fourth Row</td>
      <td>Fourth Row</td>
      <td>Fourth Row</td>
    </tr>
    <tr>
      <td>Fifth Row</td>
      <td>Fifth Row</td>
      <td>Fifth Row</td>
      <td>Fifth Row</td>
      <td>Fifth Row</td>
    </tr>
  </tbody>
</table>
```

If the first column is not persistent, just use all the same markup but without the `data-tablesaw-priority="persist"` attribute/value combination on the `<th>` element. It is totally possible to use this on more than one column or just on the 2nd, 3rd or n-th column.

After setting the table up, you may again save your draft and preview your doings in the frontend.

## Output

If you followed the markup conventions what you get should look something like this example I made a screenshot of:

![Example output inside an article](/assets/tablesaw/tablesaw-usage-screen-02.png)
