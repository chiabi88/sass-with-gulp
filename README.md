# Sass with gulp

gulp로 자동화한 sass 프로젝트 환경으로 다음과 같은 작업을 합니다.

+ html, js, image 파일 minify(js의 경우 rename되어 접미사 '.min'이 붙은 파일이 출력됩니다.)
+ sass 컴파일 (autoprefixer를 포함합니다.)
+ sassdoc (default task에 정의하지 않았습니다. `gulp sassdoc`을 입력해 task를 실행하세요.)
+ 이미지 스프라이트
+ 실시간 변경을 감시합니다.(watch)
+ BrowserSync를 통해 브라우저에서 새로고침 없이 변경 사항이 반영된(reload된, 동기화된) 페이지 화면을 확인할 수 있습니다.


※ 아래의 프로젝트 파일 구조를 준수해야합니다. (구조 변경시에는 gulpfile.js의 path 수정이 필요합니다.)

### 프로젝트 파일 구조
```
node_modules/
project/
    src/
        stylesheet/
            *.css / *.scss / *.sass
        images/
          sprites/
            *.png / *.svg / *.jpg...
        js/
        html/
    dist/
    docs/
        sassdoc/
gulpfile.js
package.json
```
(※ dist, docs 폴더는 project 폴더에 없어도 `gulp` 실행 시에 만들어집니다.)

src의 예제 파일로 `gulp` 명령어가 오류없이 실행되는지 확인해보세요. 

> **참고**
> + [gulp-sass](https://www.npmjs.com/package/gulp-sass)
>   - [A Simple Gulp’y Workflow For Sass](https://www.sitepoint.com/simple-gulpy-workflow-sass/)
>   - [Gulp 사용법 #4 (gulp-sass, gulp-sourcemaps)](http://webclub.tistory.com/470)
> + [gulp-autoprefixer](https://www.npmjs.com/package/gulp-autoprefixer)
> + [gulp.spritesmith](https://www.npmjs.com/package/gulp.spritesmith)
>   - [[걸프(Gulp)] 5. gulp.spritesmith (이미지스프라이트 만들기)](http://recoveryman.tistory.com/301)
> + [Browsersync](https://browsersync.io/docs/gulp)
>   - [Gulp 사용법 #6 (Browser-sync)](http://webclub.tistory.com/473)
>   - [크로스 브라우저 테스트에 편리한 Browsersync](https://blog.outsider.ne.kr/1216)
> + [gulp-uglify](https://www.npmjs.com/package/gulp-uglify)
>   - [[Gulp] gulp-uglify option](http://witinweb.com/post/123625188342/gulp-gulp-uglify-option)
> + [gulp-imagemin](https://www.npmjs.com/package/gulp-imagemin)
> + [gulp-htmlmin](https://www.npmjs.com/package/gulp-htmlmin)
> + [gulp-rename](https://www.npmjs.com/package/gulp-rename)
> + [del](https://www.npmjs.com/package/del)

