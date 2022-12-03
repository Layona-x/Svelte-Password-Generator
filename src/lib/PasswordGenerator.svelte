 <div class="card">
  <header class="card-header">
    <p class="card-header-title">
      Password Generator
    </p>
    <button class="card-header-icon" aria-label="more options">
      <span class="icon">
        <i class="fas fa-angle-down" aria-hidden="true"></i>
      </span>
    </button>
  </header>
  <div class="card-content">
    <div class="content">
    <div id="generate_sonuc">
      {pass_n ? password : "Herhangi Bir Şifre Oluşturulmamış"}
    </div>
      <br>
      <time datetime="2016-1-1">Please Click New Password Create</time>
      </div>
  </div>
  <footer class="card-footer">
    <a on:click={generate} href="#" class="card-footer-item">Create</a>
    <a on:click={generate_update} href="#" class="card-footer-item">Update</a>
    <a on:click={generate_delete} href="#" class="card-footer-item">Delete</a>
  </footer>
 </div>

 <script>
let password = ""
  let pass_n = false
const generatePassword = (lenght) => {
  var pass = ''; 
 var str = 'ABCDEFGHIJKLMNOPQRSTUVYZ'+'abcdefghijklmnopqrstuvwxyz0123456789@#$'
    for (let i = 1; i <= lenght; i++) { 
   var char = Math.floor(Math.random()* str.length + 1); 
   pass += str.charAt(char) 
   } 
 return password = pass
}

const generate = () => {
  if(pass_n == false){
  password = `${generatePassword(16)}`
  pass_n = true
  }else{
  alert("Zaten Bir Şifre Üretilmiş ")
  }
}

const generate_update = () => {
  if(pass_n == false){
     alert("Bir Şifre Üretilmemiş")
   }else{
     password = `${generatePassword(16)}`
  }
}

const generate_delete = () => {
  if(pass_n == false){
     alert("Bir Şifre Üretilmemiş")
   }else{
    pass_n = false
    password = "Herhangi Bir Password Üretilmemiş"
  }
}
</script>