---
title: Transition React component
components: Collapse, Fade, Grow, Slide, Zoom
---

# Transitions

<p class="description">Transitionは、UIを表現力豊かで使いやすくするのに役立ちます。</p>

Material-UIは、いくつかの基本的な [モーション](https://material.io/design/motion/) をアプリケーションコンポーネントに導入するために使用できる多くのトランジションを提供します。

サーバーレンダリングをより適切にサポートするために、Material-UIはいくつかの遷移コンポーネント（フェード、成長、ズーム、スライド）の子に `スタイル` プロパティ を提供します。 アニメーションが期待どおりに機能するには、 `スタイル` プロパティをDOMに適用する必要があります。

```jsx
// The `props` object contains a `style` property.
// You need to provide it to the `div` element as shown here.
function MyComponent(props) {
  return (
    <div {...props}>
      Fade
    </div>
  );
}

export default Main() {
  return (
    <Fade>
      <MyComponent />
    </Fade>
  );
}
```

## Collapse

子要素の上部から垂直方向に展開します。 `collapsedHeight` プロパティを使用して、展開されていないときの最小の高さを設定できます。

{{"demo": "pages/components/transitions/SimpleCollapse.js"}}

## Fade

透明から不透明にフェードインします。

{{"demo": "pages/components/transitions/SimpleFade.js"}}

## Grow

子要素の中心から外側に拡張し、同時にフェードインします。 透明から不透明へ。

The second example demonstrates how to change the `transform-origin`, and conditionally applies the `timeout` property to change the entry speed.

{{"demo": "pages/components/transitions/SimpleGrow.js"}}

## Slide

Slide in from the edge of the screen. The `direction` property controls which edge of the screen the transition starts from.

The Transition component's `mountOnEnter` property prevents the child component from being mounted until `in` is `true`. This prevents the relatively positioned component from scrolling into view from it's off-screen position. Similarly the `unmountOnExit` property removes the component from the DOM after it has been transition off screen.

{{"demo": "pages/components/transitions/SimpleSlide.js"}}

## Zoom

Expand outwards from the center of the child element.

This example also demonstrates how to delay the enter transition.

{{"demo": "pages/components/transitions/SimpleZoom.js"}}