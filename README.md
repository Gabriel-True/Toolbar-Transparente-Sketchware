# Tutoriais-Sketchware
Toolbar Transparente | Sketchware
## Criando efeito toolbar transparente no sketchware

![Print 1](https://github.com/Gabriel-True/Tutoriais-Sketchware/blob/main/Screenshot_20201025-124420.png)

### Antes de tudo temos que ativar a biblioteca do App Compat. Clique em Biblioteca › AppCompat e Design e ative-a.

![Print 2](https://github.com/Gabriel-True/Tutoriais-Sketchware/blob/main/Screenshot_20201025-124451.png)

### Feito isso, agora vamos adicionar o toolbar e status bar. Clique em Tela › Selecione a sua tela › agora adicione o Toolbar e StatusBar. Como na imagem abaixo:

![Print 3](https://github.com/Gabriel-True/Tutoriais-Sketchware/blob/main/Screenshot_20201025-124159.png)

### Agora está tudo pronto para começarmos o tutorial

1. Adicione uma linear na orientação vertical.
2. Agora adicione mais uma linear, altere o ID dessa linear para "status_bar". Como na imagem abaixo:

![Print 4](https://github.com/Gabriel-True/Tutoriais-Sketchware/blob/main/Screenshot_20201025-123638.png)

3. Agora adicione mais uma linear, e altere o ID dessa linear para "toolbar". Como na imagem abaixo:

![Print 5](https://github.com/Gabriel-True/Tutoriais-Sketchware/blob/main/Screenshot_20201025-123706.png)

### Agora vamos para os códigos
Na onCreate da sua tela, adicione os seguintes códigos dentro do bloco Adicionar Fonte Diretamente

![Print 6](https://github.com/Gabriel-True/Tutoriais-Sketchware/blob/main/Screenshot_20201025-124121.png)

### Primeiro código:

_toolbar.setBackgroundColor(Color.TRANSPARENT);

Window window = this.getWindow();

 if(Build.VERSION.SDK_INT >= Build.VERSION_CODES.LOLLIPOP) { window.addFlags(WindowManager.LayoutParams.FLAG_DRAWS_SYSTEM_BAR_BACKGROUNDS); window.addFlags(WindowManager.LayoutParams.FLAG_TRANSLUCENT_STATUS);

 window.setStatusBarColor(Color.TRANSPARENT); }
 
 ### Segundo código:
 
 ((ViewGroup)_toolbar.getParent()).removeView(_toolbar);

toolbar.addView(_toolbar);

int statusBar = getResources().getIdentifier("status_bar_height", "dimen", "android");

if (statusBar > 0) {

status_bar.getLayoutParams().height = getResources().getDimensionPixelSize(statusBar); }

toolbar.setElevation(4f);

### Pronto, agora é só compilar e veja como ficou :blush:

![Print 1](https://github.com/Gabriel-True/Tutoriais-Sketchware/blob/main/Screenshot_20201025-124420.png)
