document.getElementById("home").onclick = function () {
    displayBlock(this.id);  
    activeClass(this.id);
}

document.getElementById("educ").onclick = function () {
    displayBlock(this.id);  
    activeClass(this.id);
}

document.getElementById("expe").onclick = function () {
    displayBlock(this.id);  
    activeClass(this.id);
}

document.getElementById("proj").onclick = function () {
    displayBlock(this.id);  
    activeClass(this.id);
}

function activeClass(id) {
    document.getElementById("home").className = "inactive";
    document.getElementById("educ").className = "inactive";
    document.getElementById("expe").className = "inactive";
    document.getElementById("proj").className = "inactive";
    document.getElementById(id).className = "active";
    
}

function displayBlock(id) {
    for(let i = 1; i <= 4; i++) {
        document.getElementById("content"+i).style.display = "none";
    }
    if(forward_id(id) == "content1") {   
        document.getElementById(forward_id(id)).style.display = "grid";
    } else {
        document.getElementById(forward_id(id)).style.display = "block";
    }
    document.getElementById(id).style.transition = "all 1s";
}

function forward_id(id) {
    if(id == "home")
        return "content1";
    else if(id == "educ") 
        return "content2";
    else if(id == "expe")
        return "content3";
    return "content4";
}