 npx create-nx-workspace@latest magasiara \                                          
  --ci=github \
  --appName=groupbuying \
  --preset=react-monorepo \
  --framework=none \
  --style=none \
  --unitTestRunner=vitest \
  --e2eTestRunner=none \
  --useReactRouter=false \
  --no-interactive

npx nx serve groupbuying

npm install @mui/material @mui/icons-material @emotion/react @emotion/styled --save 
 
 npx nx g @nx/react:library packages/group-buying-card \
  --projectNameAndRootFormat=as-provided \
  --importPath=@magasiara/group-buying-card \
  --unitTestRunner=jest \
  --bundler=rollup \
  --style=none \
  --no-interactive

 npx nx g @nx/react:library button --directory packages/button --nameAndDirectoryFormat as-provided --no-interactive
 


npx nx add @nx/storybook

npx nx g @nx/react:storybook-configuration magasiara