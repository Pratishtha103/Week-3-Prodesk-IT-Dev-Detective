"how can we use hit enter in search bar input"

"<img alt="avatar image" id="avatar-image" hidden>
const avatarImage = document.getElementById('avatar-image'); 
fetch(`${url}${username}`)
            .then(res=>res.json())
            .then(data=>{
                avatarImage
            })
how do I add the data.avatar_url into avatar-image src"

"what does this error mean "level1.html:41 Uncaught (in promise) TypeError: Assignment to constant variable.
    at level1.html:41:22""

"        <a id="profile-url"></a>

            const profileUrl = document.getElementById('profile-url');
fetch(`${url}${username}`)
            .then(res=>res.json())
            .then(data=>{
                avatarImage.src = data.avatar_url;
                avatarImage.hidden = false;
                name.innerText = data.name;
                bio.innerText = data.bio;
                joiningDate.innerText = data.created_at;
                profileUrl.href = data.html_url;
            })
why isn't profile url appearing "

"for a user that isn't there, a 404 is returned by the api, how do i use this in error handling with fetch. if status===404 document.write("User not found");. where do i include this in fetch
fetch(`${url}${username}`)
            .then(res=>res.json())
            .then(data=>{
                avatarImage.src = data.avatar_url;
                avatarImage.hidden = false;
                name.innerText = data.name;
                bio.innerText = data.bio;
                joiningDate.innerText = data.created_at;
                profileUrl.href = data.html_url;
                profileUrl.innerText = "View on Github";
                profileUrl.target = '_blank';
            })
            .catch(error=> console.log(error));"

"the error message is still there after I search for a new user that exists"

"should i keep that outside fetch or inside"

"why justify center doesn not work in body tag"

"this border is visible all the time, i just want it to be visible when a profile appears
#profile-card{
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            margin-top: 20px;
            border: 2px solid #444;
            height: 400px;
            width: 400px;
            border-radius: 6px;
            font-weight: bold;
            text-align: center;
        }"

"Currently the user not found is not in the center of the div, why? 
<style>
        body{
            display: flex;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            font-family:Cambria, Cochin, Georgia, Times, 'Times New Roman', serif
        }
        input{
            width: 172px;
            height: 34px;
            border: 2px solid #444;
            border-radius: 6px;
        }
        button{
            width: 70px;
            height: 34px;
            border: 2px solid #444; 
            border-radius: 6px;
            background-color: #e5e5e5;
            color: #565656;
            font-weight:bold;
        }
        button:hover{
            background-color: #565656;
            color: #e5e5e5;
        }
        #error-message{
            color: #b90101;
        }
        #profile-card{
            display: none;
            flex-direction: column;
            align-items: center;
            justify-content: center;
            margin-top: 20px;
            border: 2px solid #444;
            height: 400px;
            width: 400px;
            border-radius: 6px;
            font-weight: bold;
            text-align: center;
        }
        #avatar-image{
            width: 100px;
            border-radius: 50%;
            overflow: hidden;
            border:2px solid black;
        }
        /* #name{

        } */
    </style>
</head>
<body>
    <h1>Dev Detective</h1>
    <form>
    <label for="username"></label>
    <input type="search" id="username"  placeholder="Enter a Github Username" name="username" autocomplete="username"> 
    <button type="submit" onclick=usernameSearch(event);>Search</button>
    </form>
    <div id="profile-card">
        <p id="loading" hidden>Loading...</p>
        <p id="error-message"></p>
        <img  src="blankprofile.png" alt="avatar image" id="avatar-image"  hidden>
        <h2 id="name"></h2>
        <p id="bio"></p>
        <h3 id="joining-date"></h3>
        <a id="profile-url"></a>
    </div>
    <script>
        function usernameSearch(event){
            event.preventDefault();
            const username = document.getElementById('username').value;
            const loading = document.getElementById('loading');
            const errorMessage = document.getElementById('error-message');
            const profileCard = document.getElementById('profile-card');
            const avatarImage = document.getElementById('avatar-image');
            const name = document.getElementById('name');
            const bio = document.getElementById('bio');
            const joiningDate = document.getElementById('joining-date');
            const profileUrl = document.getElementById('profile-url');
            //console.log('ok');
            //console.log(username);
            const url =  "https://api.github.com/users/";
            loading.hidden = false;
            errorMessage.innerText = "";
            avatarImage.src = "";
            avatarImage.hidden = true;
            name.innerText = "";
            bio.innerText = "";
            joiningDate.innerText = "";
            profileUrl.href = "";
            profileUrl.innerText = "";
            profileUrl.target = "";
            fetch(`${url}${username}`)
            .then(res=>{
                if (res.status ===404){
                    errorMessage.innerText = "User Not Found";
                    profileCard.style.display = "flex";
                    throw new error('User Not Found');
                }
                return res.json();
            })
            .then(data=>{
                profileCard.style.display = "flex";
                avatarImage.src = data.avatar_url;
                avatarImage.hidden = false;
                name.innerText = data.name;
                bio.innerText = data.bio;
                joiningDate.innerText = data.created_at;
                profileUrl.href = data.html_url;
                profileUrl.innerText = "View on Github";
                profileUrl.target = '_blank';
            })
            .catch(error=> console.log(error))
            .finally(() => {
                loading.hidden = true;
            });
        }
    </script>"

"what am i doing wrong here VM133:1 Uncaught (in promise) SyntaxError: Unexpected token '<', "<!DOCTYPE "... is not valid JSON"

"when i search for top 5 latest repository for a new user, after searching for one user, the previous repository are still visible"

"I want to add above the links top 5 latest repositories text when it appears"

"what if a user does not have any repositories"
