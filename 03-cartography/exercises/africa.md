## Resources

+ [.carto file](https://drive.google.com/file/d/0B9k_lcYQZACgY1k2RHV3MGx3MTg/view?usp=sharing)
+ image url: `https://s3.amazonaws.com/com.cartodb.users-assets.production/production/mamatablog/assets/20151025140245land_paper.png`

## Continent

+ Select Africa
+ Add analysis > Area of Influence (100 miles, 6 buffers, intact)

```css
  line-width: ramp([data_range],0.4,1,equal);
  line-color: teal;
  line-opacity: 0.5;
```

## Country

### Global styles

+ `polygon-pattern-file`
+ CartoColor `Bold`

 ```css
  polygon-pattern-file: url(https://s3.amazonaws.com/com.cartodb.users-assets.production/production/mamatablog/assets/20151025140245land_paper.png);
  polygon-pattern-opacity: 0.3;
  polygon-fill: ramp([mapcolor7], cartocolor(Bold), category(7));
  polygon-opacity: 0.2;
 ```

### Style for Africa

+ Ramp line color
+ Line offset
+ Labels

```css
 [continent='Africa']{ 
    polygon-opacity: 0.3;
    line-width: 2;
    line-color: ramp([mapcolor7], cartocolor(Bold), category(7));
    line-opacity: 0.4;
    line-offset: -1;

    ::labels  {
    text-name: [abbrev];
    text-face-name: 'Gravitas One Regular';
    text-size: 10;
    text-fill: #000;
    text-label-position-tolerance: 0;
    text-halo-radius: 0;
    text-halo-fill: #6F808D;
    text-dy: 0;
    text-allow-overlap: true;
    text-placement: point;
    text-placement-type: dummy;
    text-transform: uppercase;
    text-character-spacing: 0.5;
    text-wrap-width: 25;
}
  }
``` 

## Ocean

`@ocean: #c3d1c7;`


```css
  polygon-fill: lighten(#b3d1cf,0);
  polygon-pattern-file: url(https://s3.amazonaws.com/com.cartodb.users-assets.production/production/mamatablog/assets/20151025140245land_paper.png);
  polygon-pattern-opacity: 0.4;
```