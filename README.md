# MMM-QRCode
QRCode module for MagicMirror². Show QRCode image of encoded text.

## Screenshot
![](.github/example.png)

## Installation

In your terminal, go to your MagicMirror's Module folder:
````
cd ~/MagicMirror/modules
````

Clone this repository:
````
git clone git@github.com:MarinescuEvghenii/MMM-QRCode.git
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
			<th width="75%">Description</th>
			<th width="25%">Default value</th>
		</tr>
	<thead>
	<tbody>	
		<tr>
			<td>text</td>
			<td>The text to encode. <br /><br />For example: use the following format for WiFi network login: `WIFI:S:<SSID>;T:<WPA|WEP|>;P:<password>;H:<true|false|>;` <br />MeCard format [see wiki](https://en.wikipedia.org/wiki/MeCard_(QR_code)): MECARD:N:Doe,John;TEL:13035551212;EMAIL:john.doe@example.com;;</td>
			<td>https://github.com/basknol/MMM-QRCode</td>
		</tr>
		<tr>
			<td>colorDark</td>
			<td>Draw color</td>
			<td>"#fff" </td>
		</tr>	
		<tr>
			<td>colorLight</td>
			<td>Background color</td>
			<td>"#000"</td>
		</tr>
		<tr>
			<td>imageSize</td>
			<td>Size of the image in px</td>
			<td>150</td>
		</tr>
		<tr>
			<td>showRaw</td>
			<td>Show raw text </td>
			<td>true</td>
		</tr>		
		<tr>
			<td>hideModuleOnLoad</td>
			<td>Hide this module if you don't want to show the QR code by default. Show the module only when needed, for example using the [MMM-Remote-Control](https://github.com/Jopyth/MMM-Remote-Control) module</td>
			<td>false</td>
		</tr>	
	</tbody>
</table>