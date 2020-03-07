1.What is Template Driven form? what are the steps to create Template driven form?                          
It's suggested to use template driven form where we have small form like login form etc..               
a) Import FormsModule in app.module.ts file             
import { FormsModule }   from '@angular/forms'  
b) @NgModule({imports: [ BrowserModule, FormsModule 
c) create .ts with class   
export class login {
    constructor(
        public username: string,
        public pwd: string

    ){}
}
d) then import { login } from '../model/login';  
model = new login('Debashree','debashree');   
e)Each input element has a name property that is required by Angular forms to register the control with the form.
<form #heroForm="ngForm">
<div>
        <label for="name">User Name:</label>
        <input type="text" id="uname" [(ngModel)]="model.username" name="username" required>
      </div>

      <div>
        <label for="pwd">Password:</label>
        <input type="text" id="pwd" [(ngModel)]="model.pwd" name="pwd" required>
      </div>


