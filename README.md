# Midjourney_command

## Midjourney 란?
Midjourney는 OpenAI의 DALLE-2 및 Stable Diffusion의 DreamStudio와 같은 Text-to-Image 생성 앱으로, 수많은 이미지와 제공된 텍스트 프롬프트를 기반으로 멋진 이미지를 생성해준자.

예를 들어, “colorful flower”를 사용하면 AI가 생각하는 다채로운 꽃의 이미지를 생성하는데, 일반적으로 “coloful”과 같은 하나의 형용사만으로는 충분하지 않다. 하나의 형용사를 사용하면 AI는 일반적으로 간단한 것을 생성하기 때문에, 내가 원하는 정확한 이미지를 생성하기 위해서는 AI에게 다양한 형용사와 설명을 전달해주는 것이 좋다.

즉 “colorful flower”대신 “Beautiful flower field with flying bees and butterflies at sunset(해질녘에 벌과 나비가 날아다니는 아름다운 꽃밭)”를 사용하면 그냥 “coloful flower”를 사용한 것 보다 더 나은 결과를 얻을 수 있다.

## 프롬프트 텍스트
Midjourney 앱을 사용해 본 사람들은 텍스트에 설명이 많을수록 출력이 더 생생하고 독특하다. 초보 사용자는 일반적으로 “rabbit, moon” 처럼 간단한 텍스트로 이미지를 생성하는데, 예측 가능하고 일관된 이미지를 생성하기 위해서는 단순한 텍스트 대신 더 다양한 옵션을 사용할 수 있어야 된다.

다음은 더 나은 이미지를 생성할 수 있는 몇 가지 방법들이다.
```
Providing keywords — ‘style’(스타일 키워드 제공)
stylize(양식화)
chaos(혼돈)
Resolution(해상도)
Aspect ratio(종횡비)
passing an image as a prompt as URL(프롬프트로 이미지 URL 전달)
applying weights to the image prompts(이미지 프롬프트에 가중치 적용)
weights to the word prompts(단어 프롬프트에 가중치 적용)
filtering out words(단어 필터링)
```
### 1. 스타일 키워드 제공하기
“스타일”과 관련된 일련의 지원 프롬프트 키워드를 제공하면 선택한 스타일의 종류에 따라 다른 출력을 생성할 수 있다. 다음은 스타일로 선택할 수 있는 장르를 기반으로 하는 몇 가지 키워드와 하위 유형이다.
```
standard, japanese anime style, pixar movie style, cyber punk style, steam punk style, waterhouse style
```
아티스트를 스타일로 사용하기  
아티스트를 출력 스타일로 지정하거나, 스타일 자체를 출력 스타일로 지정할 수 있다.  
```
Andy Warhol, Da Vinci, Salvador Dali, Picasso, Vincent Van Gogh, M.C. Escher  
Surrealism(초현실주의), Cyberpunk(사이버펑크), Realism(사실주의), Cubism(입체파), Contemporary(현대), Fantasy(판타지), Abstract(추상), Impressionism(인상파), Modern, Minimal  
```
렌더링/조명 속성을 스타일로 사용하기  
컴퓨터 렌더링과 조명 속성을 출력 스타일로 지정할 수 있다.  
```
volumetric lighting, cinematic lighting, octane render, softbox lighting, glowing lights, blue lighting, long exposure, fairy lights  
```
### 2. 출력 양식화하기
--s 옵션을 사용하여 --s 700, --s 20000과 같이 스타일 설정을 추가할 수 있다. --s는 스타일을 나타내는 옵션이다.
```
/imagine babel tower --s 500
```
### 3. chaos 사용하기
--chaos는 주제의 추상화 수준을 높이거나 낮추기 위해 사용하는 옵션으로 0에서 100 사이의 숫자를 사용한다.
```
/imagine babel tower --chaos 60
```
### 4. 해상도 지정하기  
해상도를 지정하려면 8K, 4K, photorealistic, ultra photoreal, ultra details, incomate details 등과 같은 일반적인 키워드를 사용하면 된다. 또는 예측이 가능한 출력을 위해 --hd 옵션을 사용하거나, --q 옵션을 사용할 수 있어. --q 옵션은 0.25에서 2까지의 숫자를 사용한다.   
```
/imagine red rose flower --q 2
```
### 5. 종횡비 지정하기  
Midjourney의 기본 출력은 1:1의 정사각형 이미지이지만, 더 영화 같은 보기를 원하거나 PC용 월페이퍼를 만들고 싶다면 --ar 4:3, --ar 16:9와 같이 종횡비를 변경할 수 있다.  
```
/imagine babel tower --ar 4:3
```
또는 다음과 같이 사용자 정의 이미지 크기를 지정할 수도 있다.  
```
/imagine jasmine in the wild flower --w 600 --h 300
```
### 6. 프롬프트에 이미지 사용하기
이미지를 통해 해당 이미지와 유사한 이미지를 생성하고 싶다면 이미지의 URL을 사용하면 된다.  

Midjourney는 전달한 URL의 시드 이미지와 텍스트 프롬프트 모두의 데이터를 가지고 새로운 이미지를 생성해줘. 또 여러개의 이미지를 프롬프트에 전달하거나, 각 이미지에 가중치를 지정할 수도 있다.  

### 7. 이미지에 가중치 적용하기
생성된 이미지가 프롬프트에 전달된 이미지와 더 비슷하게 보이길 원한다면 –iw를 사용하여 해당 이미지에 더 높은 가중치를 부여하면 된다.  

### 8. 텍스트 프롬프트에 가중치 적용하기
프롬프트에 전달하는 텍스트에도 가중치를 부여할 수 있다.  

### 9. 이미지에서 단어 필터링하기
--no 키워드를 사용하여 원하지 않는 주제를 삭제할 수 있다.  

### 10. 흥미로운 키워드 사용하기
모든 렌즈 또는 카메라 유형  
Sony Alpha α7, ISO1900, Leica M  

세부 사항과 사실성  
photorealistic(포토리얼리스틱) , ultra photoreal(울트라 포토리얼) , ultra detailed(울트라 디테일), intricate details(복잡한 세부 사항)  

컴퓨터 그래픽  
Octane render, Unreal Engine, Ray tracing

조명 조건  
volumetric light(체적 조명), cinematic lighting(영화 조명)  

유용한 키워드들 
```
Atmospheric(분위기 있는)  
Dramatic lighting(극적인 조명)  
Anthropomorphic(의인화)  
8k  
Very detailed(매우 상세한)  
Cinematic lighting(시네마틱 조명)  
Unreal engine(언리얼 엔진)  
Octane render(옥테인 렌더)  
Photorealistic(사실적인)  
Hyperrealistic(극사실주의)  
Sharp focus(선명한 초점)  
Rim lighting(림 조명)  
Soft lighting(부드러운 조명)  
Volumetric(체적)  
Surreal(초현실적)  
Realistic CGI(사실적인 CGI)  
Fantastic backlight(환상적인 백라이트)  
HDR  
Studio light(스튜디오 조명)  
Internal glow(내부 발광)  
Iridescent(무지개 빛깔의)  
Cyberpunk(사이버펑크)  
Steampunk(스팀펑크)  
Intricate filigree metal design(정교한 금속 디자인)  
Bionic futurism(바이오닉 미래주의)  
Ray tracing(광선 추적)  
Symmetrical(대칭)  
Atompunk(아톰펑크)  
Multiverse(멀티버스)  
Concept art(컨셉 아트)  
Time loop(시간 루프)  
Maximum texture(최대 질감)  
Futurism(미래파)  
Dynamic(동적인)  
semi-realistic(반현실적인)  
```
