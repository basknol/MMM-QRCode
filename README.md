# MMM-QRCode
QRCode module for MagicMirror². Show QRCode image of encoded text.
This module is forked from: https://github.com/MarinescuEvghenii/MMM-QRCode

## Screenshot
![](.github/example.png)

## Installation

In your terminal, go to your MagicMirror's Module folder:
````
cd ~/MagicMirror/modules
````

Clone this repository:
````
git clone https://github.com/basknol/MMM-QRCode.git
````

Configure the module in your `config.js` file.

## Using the module

To use this module, add it to the modules array in the `config/config.js` file:
````javascript
modules: [
	{
		module: 'MMM-QRCode',
		header: "Scan for WiFi access", //Or for example 'Contact information'
		position: 'bottom_left',
		config: {
			// See 'Configuration options' for more information.
			text : 'https://github.com/basknol/MMM-QRCode',
			colorDark : "#fff",
			colorLight : "#000",
			imageSize : 150,
			showRaw : true,
			hideModuleOnLoad: false,
		}
	}
]
````

## Configuration options

The following properties can be configured:
<!-- why, markdown... -->
<table width="100%">
	<thead>
		<tr>
			<th>Option</th>
			<th width="100%">Description</th>
		</tr>
	<thead>
	<tbody>	
		<tr>
			<td>text</td>
			<td>The text to encode. <br /><br />For example: use the following format for WiFi network login: <code>WIFI:S:&lt;SSID&gt;;T:&lt;WPA|WEP&gt;;P:<password>;H:&lt;true|false&gt;;</code> <br /><br />MeCard format [see wiki](https://en.wikipedia.org/wiki/MeCard_(QR_code)): MECARD:N:Doe,John;TEL:13035551212;EMAIL:john.doe@example.com;;<br />				
				<br /><b>Default value:</b> <code>https://github.com/basknol/MMM-QRCode</code>
				<br />This value is <b>OPTIONAL</b>			
			</td>
		</tr>
		<tr>
			<td>colorDark</td>
			<td>Draw color<br />
				<br /><b>Default value:</b> <code>"#fff"</code>
				<br />This value is <b>OPTIONAL</b>						
			</td>
		</tr>	
		<tr>
			<td>colorLight</td>
			<td>Background color<br />
				<br /><b>Default value:</b> <code>"#000"</code>
				<br />This value is <b>OPTIONAL</b>		
			</td>
		</tr>
		<tr>
			<td>imageSize</td>
			<td>Size of the image in px<br />
				<br /><b>Default value:</b> <code>150</code>
				<br />This value is <b>OPTIONAL</b>	
			</td>
		</tr>
		<tr>
			<td>showRaw</td>
			<td>Show raw text<br />
				<br /><b>Default value:</b> <code>true</code>
				<br />This value is <b>OPTIONAL</b>	
			</td>
		</tr>		
		<tr>
			<td>hideModuleOnLoad</td>
			<td>Hide this module if you don't want to show the QR code by default. Show the module only when needed, for example using the [MMM-Remote-Control](https://github.com/Jopyth/MMM-Remote-Control) module<br />						
				<br /><b>Default value:</b> <code>false</code>
				<br />This value is <b>OPTIONAL</b>
			</td>
			</td>
		</tr>	
	</tbody>
</table>