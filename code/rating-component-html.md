### Star Rating Markup

```html
<i>{{displayText}}</i>
<div class="stars" [ngClass]="{'disabled': disabled}"> 
  <ng-container *ngFor="let star of ratings" >
    <svg title="{{star.text}}"
      height="25" width="23" class="star rating" [ngClass]="{'selected': star.stars <= _value}"
      (mouseover)="displayText = !disabled ? star.text : ''"
      (mouseout)="displayText = ratingText ? ratingText : ''"
      (click)="setRating(star)">
      <polygon points="9.9, 1.1, 3.3, 21.78, 19.8, 8.58, 0, 8.58, 16.5, 21.78" style="fill-rule:nonzero;"/>
    </svg>
  </ng-container>
</div>
```