<script>
	
    let showMsg = false
    let email=""
    let name=""
    let lastName=""
    let age=""
    const onKey = () => {
   }
    function msg () {
       alert("Your inputs " +"\n"+ 
       "Email: " + email + " \n"+
       "Name: " + name + "\n"+
       "Last Name: " + lastName + " \n" +
       "Age: " + age + " \n" +
       "Had succesfully recorded!!" 

       
       )
    }
   
</script>

<div class="container">
   <form on:submit={msg}>
       <label for="">Concentration:</label>
       <select>
           <option>BSIT Major in Bantay ng Comshop</option>
           <option>BSIT Major in Taga reformat</option>
           <option>BSIT Major in Taga ayos ng appliances</option>
           <option>BSIT Major in Taga yes yes yow!</option>
           <option>BSIT Major in Alam ayusin lahat</option>
           <option>BSIT Major in Taga ayos ng Printer</option>
       </select>
       <label for="email">Email: </label>
       <input type="email" id="email" bind:value={email} required/>
       <label for="name">Name: </label>
       <input type="text" id="name" bind:value={name} required/>
       <label for="lastname">Last Name: </label>
       <input type="text" id="lastname" bind:value={lastName} required/>
       <label for="age">Age: </label>
       <input type="number" id="age" bind:value={age} required/>
       <button>Submit</button>
   </form>

</div>

<style>
   .container {
       display: grid;
       border-radius: 10px;
       background-color:whitesmoke;
       border: 1px solid gray;
       max-width: 500px;
       height: 50vh;
       margin: 0 auto;
   }

   form {
       padding: 15px;
       
       display: grid;
       box-sizing: border-box;
       margin: 25px;

   }

   button {
       margin-top: 10px;
   }

   label {
       padding: 2px;
       font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
   }

</style>