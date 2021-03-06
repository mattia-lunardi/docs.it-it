---
title: "Procedura: Aggiungere un'animazione a una rotazione tridimensionale tramite quaternioni"
ms.date: 03/30/2017
helpviewer_keywords:
- quaternions [WPF]
- animation [WPF], 3-D translations [WPF], with quaternions
- 3-D translations [WPF], animating [WPF], with quaternions
ms.assetid: adca9cb1-066b-4de8-abbb-6b4007579ee7
ms.openlocfilehash: df51db324bffc038bc585b6d977a82d54feefb3b
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: it-IT
ms.lasthandoff: 01/23/2019
ms.locfileid: "54550929"
---
# <a name="how-to-animate-a-3-d-rotation-using-quaternions"></a>Procedura: Aggiungere un'animazione a una rotazione tridimensionale tramite quaternioni
In questo esempio illustra come animare una rotazione di un oggetto 3D tramite quaternioni.  
  
 Il codice seguente mostra una <xref:System.Windows.Media.Media3D.QuaternionRotation3D> utilizzato come valore per il <xref:System.Windows.Media.Media3D.RotateTransform3D.Rotation%2A> proprietà di un <xref:System.Windows.Media.Media3D.RotateTransform3D>.  
  
 [!code-xaml[Animation3DGallery_snip#QuaternionAnimationExampleInline1](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/QuaternionAnimationExample.xaml#quaternionanimationexampleinline1)]  
  
 Ciò <xref:System.Windows.Media.Media3D.QuaternionRotation3D> viene aggiunta un'animazione con una <xref:System.Windows.Media.Animation.QuaternionAnimation> all'interno di un <xref:System.Windows.Media.Animation.Storyboard> usando il codice seguente.  
  
 [!code-xaml[Animation3DGallery_snip#QuaternionAnimationExampleInline2](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/QuaternionAnimationExample.xaml#quaternionanimationexampleinline2)]  
  
## <a name="example"></a>Esempio  
 Il codice seguente illustra l'intero esempio.  
  
 [!code-xaml[Animation3DGallery_snip#QuaternionAnimationExampleWholePage](../../../../samples/snippets/csharp/VS_Snippets_Wpf/Animation3DGallery_snip/CS/QuaternionAnimationExample.xaml#quaternionanimationexamplewholepage)]  
  
## <a name="see-also"></a>Vedere anche
- [Cenni preliminari sull'animazione](../../../../docs/framework/wpf/graphics-multimedia/animation-overview.md)
- [Creare una scena tridimensionale](../../../../docs/framework/wpf/graphics-multimedia/how-to-create-a-3-d-scene.md)
- [Panoramica sulla grafica tridimensionale](../../../../docs/framework/wpf/graphics-multimedia/3-d-graphics-overview.md)
- [Cenni preliminari sulle trasformazioni](../../../../docs/framework/wpf/graphics-multimedia/transforms-overview.md)
- [Animare una rotazione tridimensionale usando gli storyboard](../../../../docs/framework/wpf/graphics-multimedia/how-to-animate-a-3-d-rotation-using-storyboards.md)
- [Aggiungere un'animazione a una rotazione tridimensionale usando Rotation3DAnimation](../../../../docs/framework/wpf/graphics-multimedia/how-to-animate-a-3-d-rotation-using-rotation3danimation.md)
