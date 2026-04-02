<%* 
// This file adds text in HTML and let you align it while at it.

let type = await tp.system.suggester(["None", "Heading 1", "Heading 2", "Heading 3", "Heading 4", "Heading 5", "Heading 6"], ["none", "heading1", "heading2", "heading3", "heading4", "heading5", "heading6"], true, "Which heading do you want to use?");

let align = await tp.system.suggester(["Align left", "Align center", "Align right"], ["left", "center", "right"], true, "Where do you want to align selected");

let message = await tp.system.prompt("Insert your text here", "", true, true);

let html

switch(type) {
	case "none":
		html = "<span class='" + align + "'>" + message + "</span>"
		break;
	case "heading1":
		html = "<h1 class='" + align + "'>" + message + "</h1>"
		break;
	case "heading2":
		html = "<h2 class='" + align + "'>" + message + "</h2>"
		break;
	case "heading3":
		html = "<h3 class='" + align + "'>" + message + "</h3>"
		break;
	case "heading4":
		html = "<h4 class='" + align + "'>" + message + "</h4>"
		break;
	case "heading5":
		html = "<h5 class='" + align + "'>" + message + "</h5>"
		break;
	case "heading6":
		html = "<h6 class='" + align + "'>" + message + "</h6>"
		break;
}

tR = tp.file.selection() + html;
-%>