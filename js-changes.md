# Add this In Usercustome Js 

```JAvascript
      if (localStorage.getItem("LoginStatus") == 1) {
                
                $('#profile-link').append(`<a href="#home">${localStorage.getItem('UserName')}</a>`);
            } else {
                if (localStorage.getItem("prefLang") == 'en') {
                    window.location.replace('login_en.html');
                } else {
                    window.location.replace('login_vn.html');
                }
            }
```
# Add this in doctorcustome Js 

```Javascript
      if (localStorage.getItem("LoginStatus") == 1) {
              
		          $('#profile-link').append(`<a href="view_profile_en.html">${localStorage.getItem('DoctorName')}</a>`); 
		
                
            } else {
                if (localStorage.getItem("docprefLang") == 'en') {
                    window.location.replace('doctor_login_en.html');
                } else {
                    window.location.replace('doctor_login_vn.html');
                }
            }


```
