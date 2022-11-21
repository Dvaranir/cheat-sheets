## How to import local font-faces

### You are making fonts.scss file and making mixin there like:
```scss
@mixin load-font-faces($path) {

    @font-face {
        font-family: 'Fira Sans';
        font-weight: 400;
        src: local('Fira Sans'), url(#{$path}FiraSans-Regular.ttf) format('truetype');
    }
    
    @font-face {
        font-family: 'Fira Sans';
        font-weight: 500;
        src: local('Fira Sans'), url(#{$path}FiraSans-Medium.ttf) format('truetype');
    }
    
    @font-face {
        font-family: 'Fira Sans';
        font-weight: 700;
        src: local('Fira Sans'), url(#{$path}FiraSans-Bold.ttf) format('truetype');
    }
    
}
```
### Then use it in the body of the scss file, NOT in <body> tag!!!