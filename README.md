<header>
  <script name="javascript">
    document.getElementById('loginForm').addEventListner('submit', function (e) {
        e.preventDefault()
        if (navigator.credentials) {
             var cred = new PasswordCredential({
                 id: document.querySelector('[name=username]').value,
                 password: document.querySelector('[name=password]').value,
                 name: 'User Display Name'
             });
             navigator.credentials.store(cred).then(function () {
               console.log('Credential Stored');
             });
        }
    });
  </script>
</header>
<h1> Welcome to world of quantuam </h1>
<h2> Login </h2>
<form id="loginForm" method="post">
  <input type="text" name="username" autocomplete="username"/>
  <input type="password" name="password" autocomplete="current-password"/>
  <input type="submit" value="Log In"/>
</form>
