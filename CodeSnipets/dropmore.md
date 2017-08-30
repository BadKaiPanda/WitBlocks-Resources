#Drop on braking Plant

```JAVA

		@Override
		public void onBlockDestroyedByPlayer(World world, BlockPos pos, IBlockState state) {
			EntityPlayer entity = Minecraft.getMinecraft().thePlayer;
			int i = pos.getX();
			int j = pos.getY();
			int k = pos.getZ();
   /* Random Maths Drop**/
    if ((Math.random() * 100) <= 50) {
				if (!world.isRemote) {
					EntityItem var14 = new EntityItem(world, (double) (i), (double) (j), (double) (k), new ItemStack(----------------, 1, 0));
					var14.setPickupDelay(10);
					world.spawnEntityInWorld(var14);
				}
			}

		}
```
