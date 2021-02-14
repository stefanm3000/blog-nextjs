---
title: "Explain 'this' keyword?"
date: "2021-02-14"
---

The JavaScript this keyword refers to the object it belongs to.


    let person = {

      firstName: "John",
      lastName : "Doe",
      id       : 5566,
      fullName : function() {
        return {this.firstName + 
        " " + this.lastName;}
      }
};
