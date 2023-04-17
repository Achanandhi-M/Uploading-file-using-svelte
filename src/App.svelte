<script>
    let selectedFile;
    let imageUrl;
  
    function handleFileInput(event) {
      selectedFile = event.target.files[0];
      imageUrl = URL.createObjectURL(selectedFile);
    }
  </script>
  <style>
	h1{
		padding-top: 30px;
	}
  </style>
  <center>
	<h1>Click a choose file button to upload images</h1>
  <label for="file-input">Choose a file:</label>
  <input id="file-input" type="file" on:change={handleFileInput} />
  {#if imageUrl}
    <h1>Chosen image is</h1>
    <img src={imageUrl} alt="myfile" />
  {/if}
  </center>
  