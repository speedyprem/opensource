
#Database country, State, city of world in one .sql file

I have added 3 select box for country, state, and city. Copy below code snippets to add city state country list in your web application.

```html
<form class="form-horizontal" role="form" >
	  <div class="form-group">
	    <div class="col-sm-10">
	    	<label>Select Country</label>
	        <select class="form-control" name="country" id="country">
	        <option value="0">Select Country</option>	
	        <?php
				require_once('DbConnection.php');
				$countries=mysqli_query($connection,"SELECT * FROM country ORDER BY country");
				while($country = mysqli_fetch_assoc($countries)){
					echo "<option value='".$country['id']."'>".$country['country']."</option>";
				}
			?>
	        </select>
	        <br>
	    </div>
	    <div class="col-sm-10">
	    	<label>Select State</label>
	        <select class="form-control" name="region" id="region">
	        	<option value="0">Select State</option>
	        </select>
	        <br>
	    </div>
	    <div class="col-sm-10">
	    	<label>Select City</label>
	        <select class="form-control" name="city" id="city">
	        <option value="0">Select City</option>
	        </select>
	        <br>
	    </div>
	  </div>
	</form>
```  
Get complete source code from : http://freewebmentor.com/2015/05/responsive-countrystatecity-dropdown-using-php.html

#Note: 
* All the country, state, city data and their licensing is free to use so you can use this data for any commercial or non commercial applications.

*This is a free database and dose not guarantee for complete list of world countries, states and cities and author is not responsible for this.
