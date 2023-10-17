<script>
    var name = " ";
</script>

<main>
  <form>
    <fieldset>
      <legend>Personal information</legend>

      <label for="text_input" >Enter name :</label>
      <input type="text" required bind:value={name}/>{name}

      <br /><br />

      <label for="password_input">Password :</label>
      <input type="password" required /><br /><br />

      <label for="email_input">Email :</label>
      <input type="email" required /><br /><br />

      <label for="number_input">Mobile Number :</label>
      <input type="number" min="1" max="10" step="1" required /><br /><br />

      <label for="checkbox_input">Languages :</label>
   <input type="checkbox" value="HTML" />
      <input type="checkbox" value="CSS" />
      <input type="checkbox" value="TAILWIND" /><br /><br />

      <label for="radio_input1">Male :</label>
      <input type="radio" value="option1" />

      <label for="radio_input2">Female :</label>
      <input type="radio" value="option2" /><br /><br />

      <label for="select_input">Select:</label>
      <select>
        <option>HTML</option>
        <option>HTML : 5</option>
        <option>HTML : xls</option>
      </select>
      <br /><br />

      <label for="textarea_input">Enter you previous experience with us :</label
      ><br />
      <textarea rows="4" cols="50" /><br /><br />

      <label for="date_input">Date of birth :</label>
      <input type="date" /><br /><br />

      <label for="file_input">Resume :</label>
      <input type="file" /><br /><br />

      <button>This is by BUTTON</button>
    </fieldset>
  </form>
</main>

<style>
  form {
    height: 100%;
    width: 100%;
    border: 1px solid rgb(244, 240, 32);
    /* background-color: rgb(101, 232, 81); */
    /* background-image: url(lectture); */
    text-align: justify;
  }

  fieldset {
    border: 5px double rgb(12, 23, 243);
  }

  legend {
    color: antiquewhite;
  }

  textarea {
    height: 100px;
    width: 800px;
  }

  input {
    color: rgb(226, 3, 3);
  }

  label {
    color: aliceblue;
  }
</style>
