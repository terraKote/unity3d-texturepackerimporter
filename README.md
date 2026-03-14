# Unity - Texture Packer Importer

UPM Package
---
### Install via git URL

Requires a version of unity that supports path query parameter for git packages (Unity >= 2019.3.4f1, Unity >= 2020.1a21). You can add `https://github.com/terraKote/unity3d-texturepackerimporter.git?path=Assets/TexturePacker` to Package Manager.

Authors
---
### Original tool by
* Mitch Thompson
* Harald Lurger
* Hays Clark

### Package maintainers
* Denys (terraKote) Kushnirenko

## Video Tutorial
There is a tutorial for this plugin here:
http://www.youtube.com/watch?v=CHQmvC1pqaY

## Instructions
How to import texture sheets from [Texture Packer](https://www.codeandweb.com) or [Free Texture Packer](https://free-tex-packer.com).

### TexturePacker settings:
	Data Format:  Unity3D (or JSON Hashtable, no change of extension is required)
	Allow rotation is OK
	Everything else at your discretion
	Power of 2 output textures are suggested.
	
### Unity process:
	Create a folder in your Assets/ directory for your imported sprites.
	Copy the TXT and Image file (PNG, TGA, etc) into that folder.
	Your paths should look something like:
		Assets/MySprite/MySprite.json
		Assets/MySprite/MySprite.png
			
### Shaders:
	Transparent Unlit - 
		The default shader for all imported sprite sheets.
	Opaque Unlit - 
		nontransparent tintable shader great for drawing backgrounds that don't need alpha.  Very efficient.
	Vertex Color - 
		Does not have an inspector-tweakable color property.  All colors must be set by altering the colors[] or colors32[] array of a given mesh.  
		Supports both texture alpha and vertex color alpha.
