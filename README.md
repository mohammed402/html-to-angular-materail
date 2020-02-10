# html-to-angular-materail
<div class="example-container mat-elevation-z8">
  <mat-card class="example-card">
    <mat-card-header>
      <mat-card-title><h2>Welcome <span *ngIf="loggedIn===true">{{user.firstName}} {{user.lastName}}, </span> to Angular 8 Application</h2></mat-card-title>
      <mat-card-subtitle>
        <button type="button" (click)="signInWithFB()" *ngIf="loggedIn===false" mat-flat-button color="primary">Sign In With Facebook</button>
        <button type="button" (click)="signOut()" *ngIf="loggedIn===true" mat-flat-button color="primary">Sign Out From Facebook</button>
      </mat-card-subtitle>
    </mat-card-header>
  </mat-card>
  <mat-card class="example-card" *ngIf="loggedIn===true">
    <mat-card-header>
      <mat-card-title><h2>Your Facebook Profile:</h2></mat-card-title>
      <mat-card-subtitle>Full Name: {{user.firstName}} {{user.lastName}}</mat-card-subtitle>
    </mat-card-header>
    <img mat-card-image [src]="user.photoUrl" alt="My Facebook Photo">
    <mat-card-content>
    </mat-card-content>
  </mat-card>
</div>
.example-container {
  position: relative;
  padding: 5px;
  background-color: aqua;
}
